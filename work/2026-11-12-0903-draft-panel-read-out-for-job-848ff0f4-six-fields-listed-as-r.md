# Draft panel read-out for job 848ff0f4: six fields listed as recorded, plus new charge-decode, balance and URL-shape tests to settle it in one Studio open.

**Done**

2026-11-12 09:03 UTC, spent $0.04

- https://hivemindos.app/bee/104

**Job 848ff0f4 — panel read, prepared one pass (draft)**

This is the read-out for job `848ff0f4-9370-4a6e-924f-288a07b29d83` (Episode 2 cartoon recreation, 3 shots, vertical, quote ceiling 1670 credits / $3.34). The Studio panel itself is not reachable from here, so the six fields are recorded below exactly as the visible result block stands, and the rest of this step is the decoding work that makes the single panel open settle the job in one pass. Nothing here re-runs the job.

**1. The six fields as recorded**

| # | Field | Panel value |
|---|---|---|
| 1 | Video (.mp4) | not present in the recorded result |
| 2 | Poster image | one unlabelled jpeg — `https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/ea9cb3d1-b005-4a21-9e73-3e84f662f1e8.jpeg` (role not stated: poster, frame, or placeholder) |
| 3 | Contact sheet | not present |
| 4 | Duration (s) | not present |
| 5 | audioPeak | not present |
| 6 | Settled charge | not present — no credits, no USD |

**2. New: decode table for the settled charge**

Rate is exactly 500 credits = $1.00 (shot $1.08 = 540 credits; assembly $0.10 = 50 credits). So one charge reading identifies the billing directly, and one balance reading cross-checks it. Quote-time balance was **1340.976 credits**, so post-job balance = 1340.976 − settled credits.

| Settled credits | USD | Implied billing | Implied post-job balance |
|---|---|---|---|
| 0 | $0.00 | nothing chargeable | 1340.976 |
| 50 | $0.10 | assembly only | 1290.976 |
| 540 | $1.08 | 1 shot | 800.976 |
| 590 | $1.18 | 1 shot + assembly | 750.976 |
| 1080 | $2.16 | 2 shots | 260.976 |
| 1130 | $2.26 | 2 shots + assembly | 210.976 |
| 1620 | $3.24 | 3 shots, no assembly | −279.024 |
| **1670** | **$3.34** | **3 shots + assembly (maximum)** | **−329.024** |

Any figure not on this table means a billing component that is not a whole shot or the assembly — worth quoting verbatim if so.

**3. New: one reading falsifies another**

Of the eight rows, only the last two are negative — and both are 3-shot billings. Therefore:

- **Post-job balance ≥ 0 ⇒ fewer than 3 shots were billed.** A full three-shot job billed at 1620–1670 credits must drive the balance to about −279 to −329. So a positive balance and a had-it-all-been-billed charge cannot both be true.
- **Post-job balance < 0 ⇒ every shot was billed**, and the magnitude names the count: about −279 (no assembly), −329 (with assembly).
- **Settled USD × 500 must equal settled credits exactly.** If they differ by even one cent/credit, one of the two numbers is misread.
- **Charge of 1130 credits / $2.26 is the Episode 3 total** (2 shots + assembly), not this job's maximum — if that figure appears, the panel is showing the wrong job's settlement or only two shots were billed.

**4. New: duration and balance read together distinguish a real assembly**

At ~5.042s per shot (Episode 3: 2 shots, 10.1s):

- **~15.1s with a negative balance and 1670/$3.34** → genuine 3-shot assembly, fully billed. The record is consistent and the job is settled.
- **~15.1s with balance ≥ 0** → the video exists but the billing missed shots; a settlement error, not a production error.
- **~10s** → two shots assembled; the third is missing, and 1130/$2.26 is the matching charge.
- **~5s** → one shot only; 590/$1.18 matches. No assembly happened.
- **duration absent and audioPeak absent** → the panel agrees with the thin record; the jpeg is the sole artifact and 0 credits is the correct charge.
- **audioPeak present but duration absent** (or the reverse) → one field was captured and the other dropped; note which, because audioPeak implies a produced mux, not a still.

**5. New: the URL-shape test on whatever .mp4 appears**

- The single recorded output sits on **paid-agent-gateway** at `/api/media/managed/outputs/<uuid>.jpeg` — an image-shaped path, the same shape as the mascot reference sheet. Episode 3's finished assets all sit on **studio-gateway** at `/v1/outputs/`.
- If the panel's .mp4 is on **studio-gateway `/v1/outputs/`**, that is the expected video-production shape and the earlier record was simply missing outputs.
- If the .mp4 sits on **paid-agent-gateway `/api/media/managed/outputs/`**, the video was surfaced on the image path; note it.
- If the .mp4's uuid is **the same `ea9cb3d1-b005-4a21-9e73-3e84f662f1e8`** as the jpeg, one asset has been republished under two extensions — a placeholder, not a video. A different uuid means a separate file.

**6. What I could not confirm from here**

Fields 1, 3, 4, 5 and 6 are absent from the recorded result; field 2 exists as a file but its role is unlabelled and I cannot fetch it to check pixel dimensions (a 9:16 frame would be ~1080×1920; a contact sheet or a landscape still would not). The earlier withinBudget mismatch — the 1670 ceiling exceeding the 1340.976 quote-time balance by 329.024 credits while still reporting `withinBudget: true` — stands unresolved, and the table in §2 shows why: three billed shots put the balance negative by exactly that 329.024 credits. This step is a draft read-out; nothing here runs or posts.

**Left for the owner:** open `848ff0f4-9370-4a6e-924f-288a07b29d83` in Hivemind Studio once and read the six fields off the panel — with §2–§5 above, that single reading settles the charge, the billing, the shot count and the asset question at once.
