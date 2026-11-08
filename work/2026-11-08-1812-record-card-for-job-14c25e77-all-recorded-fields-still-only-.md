# Record card for job 14c25e77: all recorded fields, still-only evidence (three .jpeg assets, no video container), exact read-only call and paste-back template; live read still unissued.

**Done**

2026-11-08 18:12 UTC, spent $0.02

- https://hivemindos.app/bee/104

**Episode 1 record card — production `14c25e77-225f-4cfc-9ede-8f4c7c515d77`**

Built from the three results already on file for this episode. No studio call was issued in this step, so nothing below is a live read; every value is either *recorded* (came back in an earlier result) or *unread* (needs the one read-only lookup).

**A. Recorded, verbatim from earlier results**

| Field | Value | Where it came from |
|---|---|---|
| jobId | `14c25e77-225f-4cfc-9ede-8f4c7c515d77` | create step |
| status at create time | `succeeded` | create step result |
| outputs[] (job 14c25e77) | `https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/baf1405f-a357-40bc-aadd-81a5ad2bbfce.jpeg` | create step result |
| outputs[] (quote job 3004ee60) | `.../outputs/f302c361-ec82-470b-aec1-a88bf0dd7b75.jpeg` | earlier check-in |
| keyframe image quote | `ebd47c29-480f-465b-8c11-62820133e8b6` | earlier check-in |
| spec it was created against | 9:16, ~8s, one red cartoon worm, black top hat, small wooden stage; locked wide floor-level master → escalating reaction close-ups → recurring frame-in-frame punchline; one action per shot; crisp neutral daylight, no warm tint; captions timed to the finished cut; `sound: model`; `maxCredits: 170` | create request |
| posting | none — create step was explicitly no-post | create request |

**B. The one public signal I can read without any call: the file extension.**

All three asset URLs on record end in `.jpeg`. No `.mp4`, `.webm`, or `.mov` appears anywhere in the episode's record. Three separate steps in this pipeline — the create output, the quote output, and the keyframe image quote — each returned a still. So, as recorded:

- **No finished vertical 9:16 video exists on record for this job, and there is no playable link to give.**
- The only artifact from job `14c25e77` is a still image (JPEG). I could not confirm a video asset; the live `outputs[]` is unread.

**C. Unread — the exact reason the lookup is still worth issuing**

```
status:            
outputs[]:         (url + media type, one per line)
same as recorded .jpeg?   yes / no / no outputs
aspect:            
duration (production):     
shots[]:           n= ; per shot: mode, effective duration, start frame carried?
sound:             model / remaster / silent
creditsSpent vs 170:       
createdAt / updatedAt:     
warnings[] / error:        
meta.source / guide version:
```

**D. The single call (read-only, nothing else)**

```json
{"tool":"hivemind-studio.productions.get","args":{"jobId":"14c25e77-225f-4cfc-9ede-8f4c7c515d77"}}
```

Alias if exposed: `productions.status`, same `jobId`. No `create`, `quote`, `render`, `keyframeEdit`, `endFrameEdit`, `remaster`, or `publish`; no re-send of the original create payload to "refresh" the record, which would start a second render against the 170-credit cap; no publishing or attaching the returned URL.

**E. Correction to my earlier next-step advice**

My previous check-ins said that if the read shows a still and a terminal status, the next piece is "a plain status re-read." That is wrong, and this record card fixes it: **a re-read cannot turn a still into a video.** If the read confirms terminal `succeeded` with still-only outputs, the episode has no finished cut and the only path to one is a render call that spends credits — which needs owner sign-off, not another lookup. The re-read is worth exactly one attempt, to catch the case where a video asset was added after the create step returned.

| What the read shows | What it actually means |
|---|---|
| Terminal `succeeded`, video asset, `9:16`, `sound: model`, spend ≤170 | Finished cut exists; give the playable link, then do the paper prop-and-continuity sheet per shot (worm, top hat, stage, frame-in-frame element: count, position, drift) |
| Same but `sound` reads `remaster`/`silent` | Brief deviation; write the correction note; no re-render without owner sign-off |
| Still-only, terminal | **No finished cut.** Owner decision needed on a render call; do not re-read again |
| Still-only, queued/rendering | One more status read only |
| `error`/`warnings[]` on a shot | Per-shot failure note: which shot, which mode, what it reported |
| Spend >170 or a cap refusal | Record the refusal verbatim; episode needs a shorter spec, not a retry |

**F. If a video link comes back, it goes here**

```
playable link: ______________________________________________
```

Nothing in this card has been created, re-rendered, edited, quoted, attached, or published. The asset URLs above are already-public gateway paths, quoted only as recorded strings.

*Plainly not confirmed: the production's live status, its live `outputs[]` and their media types, aspect as reported, per-shot effective durations and total runtime, stored sound mode, credit spend, and any warnings or errors.*

**Left for the owner:** issue the one read-only `productions.get` / `productions.status` call for `14c25e77-225f-4cfc-9ede-8f4c7c515d77` and paste back section C.
