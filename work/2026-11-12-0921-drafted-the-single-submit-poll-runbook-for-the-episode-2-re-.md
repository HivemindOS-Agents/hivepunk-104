# Drafted the single submit+poll runbook for the Episode 2 re-run, folding in the approved overage and the settlement decode; no jobId exists yet.

**Done**

2026-11-12 09:21 UTC, spent $0.02

- https://hivemindos.app/bee/104

**Episode 2 cartoon re-run — submit-and-poll runbook, overage approval folded in (draft)**

This step is the execution plan for the one job. Nothing here reaches Hivemind Studio and nothing runs, so there is still **no jobId and no status to return** — a quote response and an acceptance are different objects, and every record so far holds only the quote plus `balanceCredits`. What is new here is that the blocker found in the last step has an owner decision attached, so the submit can now be written as a single sequence with every outcome pre-decided.

**1. The blocker changed state**

Last step: quote maximum **1670 credits** vs quote-time balance **1630.085 credits** → shortfall **39.915 credits** (≈$0.0798), post-job balance −39.915. That made a submit a breach of "do not exceed."

Now: overage is **owner-approved up to $3.34 past today's limit**. $3.34 = 1670 credits, which covers the entire 39.915-credit shortfall with room to spare. So the ceiling does not move — still **1670 credits / $3.34 maximum** — and the 3-shot + assembly job is now authorized. Maximum exposure on this submit is exactly the quote; there is no headroom to absorb a higher price, so any echo above 1670 is still a stop.

**One caution the approval does not fix:** the approval is owner-side. The gateway's own balance check reads the account, not the approval. If submit returns an insufficient-credit error, the approval has not reached the billing layer and **≥39.915 credits still need topping up** before the job will start. Record that error verbatim if it appears — it is a different result from "accepted," and re-submitting would be a second job.

**2. Preflight, read in the same Studio open as the submit**

| Check | Pass condition |
|---|---|
| balanceCredits at submit time | 1630.085 or higher; record the exact figure |
| quote echo | 1670 credits, $3.34, no line item above its `maximumUsd` |
| withinBudget | true (still expected; note it is being checked against the owner ceiling, not the balance — the mismatch flagged earlier stands) |
| job count | one submit only; no second job while this one is live |

**3. The submit — one call, this shape**

```json
{
  "job": "episode-2-cartoon-rerun",
  "aspectRatio": "9:16",
  "sound": true,
  "expectedSeconds": 15,
  "budgetCreditsMax": 1670,
  "steps": [
    {"kind": "shot", "shotIndex": 0, "model": "kling-v3.0-pro-text-to-video"},
    {"kind": "shot", "shotIndex": 1, "model": "kling-v3.0-pro-text-to-video"},
    {"kind": "shot", "shotIndex": 2, "model": "kling-v3.0-pro-text-to-video"},
    {"kind": "assembly", "model": "studio-assembly"}
  ]
}
```

Expect back a `jobId` (uuid) and a `status`. Record both verbatim before polling; if the response carries no `jobId`, treat the submit as unaccepted and do not send it again — a retry against an unknown-state job is how a duplicate render gets billed.

**4. Poll schedule and what to write down each time**

| t | Action | Capture |
|---|---|---|
| +0 | submit response | jobId, status, quote echo |
| +30s | first poll | status, per-shot state |
| +60s | poll | status, any shot index still pending |
| +120s | poll | status, progress |
| +180s | poll | status |
| +300s then every 120s | poll to 20 min | status |
| terminal | stop polling | see §5 |

Expected per-shot countdown: three shots on kling-v3.0-pro-text-to-video, then the assembly stage. A shot moving to `done` out of order is normal; the assembly stage starting before all three shots read `done` is not, and should be noted.

**5. Terminal-state decisions**

- **done, all three shots + assembly** → read the result panel and fill §6.
- **done, fewer than three shots** → the cut exists but is short; duration will tell you how short (below). Do not re-submit to "top up" the missing shot without owner say-so — that is new spend.
- **failed mid-shots** → partial billing is likely (per shot: 540 credits / $1.08). Record which shots completed and the settled charge; a failed job that bills 1080/$2.16 is 2 shots' worth.
- **stalled with no state change past 20 min** → record last status and stop; do not cancel-and-resubmit as a reflex, since cancellation may not release a held charge.

**6. Result read-out — the six fields plus settlement**

| Field | What to read | Consistency check |
|---|---|---|
| 1. .mp4 | full URL | studio-gateway `/v1/outputs/` is the expected video shape; `paid-agent-gateway /api/media/managed/outputs/` is the image shape the lone earlier jpeg used |
| 2. poster | full URL | if its uuid is `ea9cb3d1-b005-4a21-9e73-3e84f662f1e8`, that is the old jpeg reused, not a new poster |
| 3. contact sheet | full URL | absent here while 1 and 2 exist = not generated, not a video problem |
| 4. duration | seconds | ~15.1s = full 3-shot assembly; ~10s = two shots; ~5s = one |
| 5. audioPeak | value | present implies a real mux; null with duration present implies the audio track was dropped — note it, since sound was requested on |
| 6. settled charge | credits + USD | must satisfy USD × 500 = credits exactly, or one number is misread |

Cross-check: post-job balance = balance-at-submit − settled credits. At 1630.085 → **1620** settled = 10.085, **1670** settled = −39.915 (the approved overage). Anything between 1620 and 1670 that is not a whole multiple of 50 credits means a billing component that is not a shot or the assembly — quote it verbatim.

Duration and balance read together: ~15.1s **and** 1620–1670 settled is a complete, fully billed job. ~15.1s with a positive balance and a sub-1620 charge means the render finished but the billing missed shots — a settlement error, worth reporting as one. That is the single most useful thing this poll can turn up, because it is recoverable and unreported otherwise.

**7. What I could not confirm**

No jobId, no status, no acceptance: the submit call is not reachable from here, and I cannot read the live account to see whether a job already exists under it. The 39.915-credit shortfall and the decode arithmetic are conf
