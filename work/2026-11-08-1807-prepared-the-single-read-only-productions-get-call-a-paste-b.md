# Prepared the single read-only productions.get call, a paste-back field template, a decision table, and a caption-timing worksheet; live status unconfirmed.

**Done**

2026-11-08 18:07 UTC, spent $0.02

- https://hivemindos.app/bee/104

**One read-only studio lookup: the call, the paste-back, and what to do with each answer**

**1. The single call (read-only, nothing else)**

```json
{"tool":"hivemind-studio.productions.get","args":{"jobId":"14c25e77-225f-4cfc-9ede-8f4c7c515d77"}}
```

Alias if the studio exposes it: `productions.status`, same `jobId`, same read, no side effects. No `create`, `quote`, `render`, `keyframeEdit`, `endFrameEdit`, `remaster`, `publish`. No re-send of the original create payload to "refresh" the record — that would start a second render against the 170-credit cap.

**2. What I could not confirm**

I cannot issue the call in this step, so the production's live status, assets, durations, spend and whether the finished cut is delivered as video are all **unread by me**. Everything in §3–§5 is either a template or a rule for reading the answer, not the answer.

**3. Paste-back template — copy these fields from the response, nothing else**

```
status:            
outputs[]:         (url + media type, one per line)
outputs same as recorded .jpeg?   yes / no / no outputs
aspect:            
duration (prod):   
shots[]:           n=  ; per shot: mode, eff. duration, start-frame carried?
captions:          present? y/n ; total slots:
sound:             model / remaster / silent
creditsSpent vs 170:
createdAt / updatedAt:
warnings[] / error:
meta.source / guide version:
```

The unresolved flag from earlier check-ins: the create step returned a path ending `.jpeg` (`.../baf1405f-a357-40bc-aadd-81a5ad2bbfce.jpeg`). Whether `outputs[]` now lists a **video** asset for the finished cut, or still that still image, is exactly what this read settles. I have not settled it.

**4. Decision table — one read, one next move (all paper, no renders)**

| What the read shows | Next piece of work |
|---|---|
| Terminal `succeeded`, video asset, `9:16`, `sound: model`, spend ≤170 | Prop-and-continuity sheet per shot (worm, top hat, stage, frame-in-frame element: count, position, drift between shots) — paper only |
| Same, but `sound` reads `remaster`/`silent` | Flag as brief deviation; write the correction note; do not re-render without owner sign-off |
| Asset is the `.jpeg` still, no video | Plain status re-read next check-in; nothing else |
| Status queued/rendering | Plain status re-read next check-in; nothing else |
| `error`/`warnings[]` on a shot | Per-shot failure note; list which shot, which mode, what it reported |
| Spend >170 or a refused-cap message | Record the refusal verbatim; the episode needs a shorter spec, not a retry |

**5. New piece of work: caption timing worksheet keyed to the finished cut**

Captions must be timed to the cut that exists, not to the spec. Rule: read each shot's **effective** duration, take the cumulative sum as each caption's start, and place the next start at that sum. Do not use requested lengths.

Worked slot map at the nominal plan (replace every number with the effective `duration` once read):

| Shot | Requested | Slot start (from cumulative) | Caption rule |
|---|---|---|---|
| 1 wide master, floor level | 2.0s | 0.00 | enter 0.15s after cut, clear before shot end |
| 2 reaction close-up | 2.0s | = eff(1) | one line, ≤ shot length − 0.3s |
| 3 reaction close-up, escalated | 2.0s | = eff(1)+eff(2) | one line, ≤ shot length − 0.3s |
| 4 frame-in-frame punchline | 2.0s | = eff(1)+eff(2)+eff(3) | land on the beat, hold to end − 0.4s |

Guard: total of effective durations is the true runtime; if it drifts past the ~8s brief, rescale caption text lengths, not the cut. H3-family shots come back slightly longer than asked (per the studio guide noted in my first check-in), which is why requested numbers must not be trusted for this sheet.

**6. Read-only guardrails**

No edits, no re-quote, no second render, no publishing or attaching the returned URL anywhere — the create step was explicitly no-post and this lookup inherits it. Return only the reported fields.

*Plainly not confirmed: live status, assets, durations, credit spend, sound mode, and whether the delivered cut is video.*

**Left for the owner:** issue the one `productions.get` call for `14c25e77-225f-4cfc-9ede-8f4c7c515d77` and paste back the §3 fields; I will fill the caption sheet and run the §4 branch.
