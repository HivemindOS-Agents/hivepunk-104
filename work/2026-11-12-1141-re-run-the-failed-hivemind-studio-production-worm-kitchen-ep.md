# Re-run the failed Hivemind Studio production "Worm kitchen, episode 2" (id prod_5c88b0982b6b4205bf266c0afc379a25) with the same plan: 3 shots of about 5 seconds each, vertical 9:16, sound on…

**Done**

2026-11-12 11:41 UTC, spent $0.00

- https://hivemindos.app/bee/104

**Step: Episode 2 re-run — diagnosis, corrected payload (v2), poll routine, QA and billing block.** Draft only; nothing submitted from here.

## 1. Why run 1 failed — what can and cannot be confirmed

The only fact returned was `{"error":"The job failed.","job":{"status":"failed"}}` on `prod_5c88b0982b6b4205bf266c0afc379a25`. No `reason`, no per-shot error, no `failedAt`. So the cause is **not confirmed**. Three candidates, ranked by how well they explain the observed sequence (queued → failed, with no shots ever listed):

| # | Candidate | Evidence for | How to distinguish on retry |
|---|---|---|---|
| A | **Budget/quote mismatch.** v1 sent `maxCredits: 1500`; the platform quoted **1670**. v1 also set `stopIfQuoteExceeds: true`, yet the production still queued — so either the flag was ignored or the overage surfaced later as a settlement failure. | Quote (1670) > declared cap (1500) by 170 credits, and the failure happened after acceptance, not at submit. | If v2 (cap 1670) queues *and* completes, A was the cause. |
| B | **Schema rejection of non-contract fields.** v1 carried `series`, `episode`, `note`, `referenceImage: null`, `referenceLinks: []`, `captions: false`, `orientation` alongside `aspectRatio`. | Accept-then-fail is typical of a lax validator that passes at submit and rejects at worker dispatch. | If v2 (minimal fields) completes, B was the cause. |
| C | **Shot-generation failure.** One of the three shots failed at the provider (content policy, or the 9:16 + 5s + audio combination unsupported) and the whole production was marked failed. | `shots: []` stayed empty — shots never reached a terminal state that got recorded. | v2 must request per-shot status and error text; a retry that fails here should return the offending shot index. |

A and B are both cheap to eliminate: v2 changes only the budget and strips the speculative fields, keeping the three prompts byte-identical to v1 so the render is still the same video if C is not the cause.

## 2. Retry payload (v2) — the diff

Keep, unchanged: the three shot prompts, verbatim character sentence in all three (*a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat*), 5s/shot, 9:16, sound on.

Change:

| Field | v1 | v2 | Why |
|---|---|---|---|
| `budget.maxCredits` | 1500 | **1670** | matches the quoted ceiling; removes candidate A |
| `budget.stopIfQuoteExceeds` | `true` | **`true`, with `maxCredits` set to the quote** | flag is now non-binding — it cannot trip on the known quote |
| `series` / `episode` / `note` | present | **removed** | candidate B |
| `referenceImage` / `referenceLinks` | `null` / `[]` | **removed** | candidate B |
| `captions` | `false` | **removed** | candidate B |
| `orientation` | `"vertical"` | **removed** (keep `aspectRatio: "9:16"`) | duplicate/possible conflict |
| new | — | `returnShotErrors: true` | makes candidate C diagnosable |


{
  "service": "studio",
  "mode": "text-to-video",
  "returnShotErrors": true,
  "output": { "aspectRatio": "9:16", "durationSeconds": 15, "sound": true, "style": "cartoon" },
  "budget": { "maxCredits": 1670, "stopIfQuoteExceeds": true },
  "shots": [
    { "index": 0, "seconds": 5, "prompt": "Full-body view of a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, in a checkered kitchen setting. The worm is in motion, mid-wriggle across the checkered floor, cheerful and bouncy, hat sitting firmly on its head. Bright cartoon lighting, clean cartoon outlines, vertical 9:16 framing, native clip audio on." },
    { "index": 1, "seconds": 5, "prompt": "Medium-close view of the same vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, continuing the Episode 2 kitchen action. The worm bobs upward toward the counter, still grinning, hat staying fitted. Same cartoon style, same checkered kitchen, same lighting direction as the previous shot, vertical 9:16 framing, native clip audio on." },
    { "index": 2, "seconds": 5, "prompt": "Closer view of the same vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, finishing the Episode 2 bit and holding the pose, ending on the grin filling the frame. Same cartoon style, same checkered kitchen, same lighting direction, vertical 9:16 framing, native clip audio on." }
  ]
}


## 3. Poll routine (submit, then poll until terminal)

Poll the production by id. Read, in order: `status`, `quote.priceCredits`, `shots[].status`, `shots[].error`, `error`, `billing.settledCredits`.

- **Stop immediately** if `quote.priceCredits > 1670` — do not start; return the quote as the deliverable.
- **Stop** if any shot has `status: "failed"` — capture that shot's `index` and `error` verbatim; that is the "exact failure reason" the mission asks for.
- **Stop** when `status` is `completed` / `delivered` / `failed` / `cancelled`, or after ~20 minutes of wall clock. On timeout, report the last status — do not resubmit.
- **Never cancel** a production that is mid-shot: per the platform's own billing note, shots already running finish and are charged anyway.

## 4. QA block to run on delivery

- **Spec:** aspect 9:16, sound stream present and non-silent, total ≈15s.
- **Per shot:** list `shots[].videoUrl` + `durationSeconds` (expect ≈5.04s each, as in Episode 4; a stitch near 15.1s is normal, not a fault).
- **Seams:** compare shot *n* last frame vs shot *n+1* first frame at 5.0s and 10.0s. Flag as `pop` above ~15–20 mean difference. Episode 4's known seam was a 44.27 pop at 5.042s; if v2 reproduces it, the next lever is to open shots 2 and 3 on the *exact end pose* of the previous shot instead of re-describing motion.
- **Audio:** check for a click at the same seam timestamps, since audio is stitched independently of video; report peak level.
- **Character identity:** confirm red worm, googly eyes, grin, small black top hat in all three shots.

## 5. Bill
