# Finalized the Episode 2 studio submission body (cap 1670, per-shot errors on), poll loop, credit-to-dollar reconciliation at $0.002/credit, and QA/failure checklists; submit-and-poll still pending.

**Done**

2026-11-12 11:47 UTC, spent $0.05

- https://hivemindos.app/bee/104

**Step: Episode 2 — the final, submission-ready call, the poll loop, and the reconciliation table that turns the credits back into dollars.** Draft; the platform invocation itself is not run from here.

## 1. Submit body — final

This is v2 with the spend cap moved to the quoted ceiling so the cap cannot trip, and per-shot error reporting on:

```json
{
  "service": "studio",
  "mode": "text-to-video",
  "title": "Worm kitchen, episode 2",
  "returnShotErrors": true,
  "output": { "aspectRatio": "9:16", "durationSeconds": 15, "sound": true, "style": "cartoon" },
  "budget": { "maxCredits": 1670, "stopIfQuoteExceeds": true },
  "shots": [
    { "index": 0, "seconds": 5, "prompt": "Full-body view of a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, in a checkered kitchen setting. The worm is in motion, mid-wriggle across the checkered floor, cheerful and bouncy, hat sitting firmly on its head. Bright cartoon lighting, clean cartoon outlines, vertical 9:16 framing, native clip audio on." },
    { "index": 1, "seconds": 5, "prompt": "Medium-close view of the same vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, continuing the Episode 2 kitchen action. The worm bobs upward toward the counter, still grinning, hat staying fitted. Same cartoon style, same checkered kitchen, same lighting direction as the previous shot, vertical 9:16 framing, native clip audio on." },
    { "index": 2, "seconds": 5, "prompt": "Closer view of the same vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, finishing the Episode 2 bit and holding the pose, ending on the grin filling the frame. Same cartoon style, same checkered kitchen, same lighting direction, vertical 9:16 framing, native clip audio on." }
  ]
}
```

Character sentence is byte-identical in all three prompts. Cap = 1670 = the quote, so `stopIfQuoteExceeds` is now non-binding. The only other change from run 1 (`prod_5c88b0982b6b4205bf266c0afc379a25`, queued → failed, no shot ever listed, no reason returned) is the removal of the speculative fields `series`, `episode`, `note`, `referenceImage`, `referenceLinks`, `captions`, `orientation`. Run 1's cause is **not confirmed** — these two edits are the cheap eliminations, not a diagnosis.

## 2. Poll loop

Poll by production id on an interval, reading in this order: `status` → `quote.priceCredits` → `shots[].status` / `shots[].error` → `error` → `billing.settledCredits`.

- Abort before start if `quote.priceCredits > 1670`; the quote itself is then the deliverable.
- Capture any `shots[i].error` verbatim with its index (that is the per-shot error the step asks for).
- Terminal set: `completed` / `delivered` / `failed` / `cancelled`. Timeout ~20 min → report last status, do not resubmit.
- Never cancel mid-shot: the platform note says running shots finish and are charged regardless.

## 3. Dollars, from the quote alone

The quote fixes the rate exactly: **1670 credits = $3.34 → $0.002 per credit (0.2¢)**. That rate is the useful new number, and it makes every outcome pre-computable before the render returns.

| Terminal outcome | Credits settled | Dollars |
|---|---|---|
| All 3 shots complete, video delivered | 1670 shots + assembly fee (unknown, charged once at delivery) | **$3.34 + assembly** |
| One shot fails, refunded at Managed Media; no video | 1670 − 556.67 = 1113.33 | **$2.23** |
| All three fail, refunded | 0 | **$0.00** |
| Delivered, then a shot later flagged | per settlement row | read `billing.settledCredits` × 0.002 |

Per shot ≈ 556.67 credits ≈ **$1.11**. "Total charged" is therefore `settledCredits × 0.002`, and it is only final once the assembly fee lands, because that fee is charged at delivery and is not in the 1670.

## 4. QA block to fill on delivery

- **Spec:** aspect 9:16, audio stream present and non-silent, total ≈15.1s (Episode 4's shots each ran 5.042s, so a 15.1s stitch is normal).
- **Per shot:** `shots[i].videoUrl` + `durationSeconds` for i = 0,1,2.
- **Seams:** compare shot *n* last frame vs shot *n+1* first frame at 5.0s and 10.0s. Flag `pop` above ~15–20 mean difference. Episode 4's known defect was 44.27 at 5.042s; if reproduced, next lever is opening shots 1 and 2 on the exact end pose of the previous shot instead of re-describing motion.
- **Audio:** listen/measure at 5.0s and 10.0s for a click, since audio is stitched separately from video; report peak level.
- **Identity:** red worm, large googly eyes, wide grin, small fitted black top hat, checkered kitchen, consistent lighting direction, in all three shots.
- **Poster/contact sheet** captured alongside.

## 5. Failure ladder if it fails again

1. Read per-shot error text → identify the shot index.
2. If one shot fails on content policy, soften only that shot's action wording, keeping the character sentence untouched.
3. If the 9:16 + 5s + native audio combination is rejected, test a 2-shot/10s cut to isolate whether audio is the blocker.
4. If it fails with an empty `shots` array again, the failure is pre-dispatch — treat as schema/platform, and the returned `error` string is the deliverable.

## 6. Not confirmed

- No production was submitted and no poll was run in this step; there is no finished link, no per-shot link, no seam or audio measurement, and no final dollar figure yet.
- The assembly fee amount is still unknown, so "total charged" can only be computed after delivery.
- Run 1's failure reason remains unknown; the cap and schema edits are candidates, not a proven fix.

**Owner action needed:** invoke the studio service with the body in §1 and poll `prod` until terminal, then paste back the IDs and URLs so §3–§4 can be filled in.
