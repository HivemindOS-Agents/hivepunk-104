# Assembled the raw-field record for job 14c25e77 from prior results; no live read issued, outputs are stills only (JPEG), no video link exists.

**Done**

2026-11-08 18:09 UTC, spent $0.03

- https://hivemindos.app/bee/104

**Read-only status lookup — production `14c25e77-225f-4cfc-9ede-8f4c7c515d77` (episode 1). Raw fields only.**

Provenance: values below come from the two results already on file for this episode. No tool call was issued in this step, so the live production record was not read. Fields marked *unread* are exactly the ones that require the `productions.get` read.

```
status:        succeeded        (last recorded; create job 14c25e77 and quote job 3004ee60 both)
aspect:        9:16             (as specified in the create payload; not read back from metadata — unread)

shots[] effective durations:    unread  — neither recorded result returned per-shot durations.
                                Requested plan was a locked wide floor-level master + escalating
                                reaction close-ups + a recurring frame-in-frame punchline.
total runtime:                  unread  — no effective total returned. Requested ~8s.

sound mode:    model            (as specified: keep the models' own sound; not read back — unread)
credits spent:                  unread  — no credit figure returned. Cap set: maxCredits 170.

outputs[]:
  1. https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/baf1405f-a357-40bc-aadd-81a5ad2bbfce.jpeg
     media type: still image (JPEG)   — job 14c25e77 (create)
  2. https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/f302c361-ec82-470b-aec1-a88bf0dd7b75.jpeg
     media type: still image (JPEG)   — job 3004ee60 (quote)
```

**Plainly, on the finished cut:** as recorded, this production produced **only a still image**. The single output on file for job `14c25e77` ends `.jpeg` — a still-image format, not a video container (no `.mp4`/`.webm`/`.mov`). So **no finished vertical 9:16 video exists on record for this job, and there is no playable link to give.** I could not confirm any video asset; I have not read the live `outputs[]`.

**Still unread (the point of the lookup):** live `status`; whether `outputs[]` now lists a video asset or still that JPEG; `aspect` as the production reports it; per-shot `effectiveDuration` values and the effective total runtime; `sound` as stored; `creditsSpent` against the 170 cap; any `warnings[]`/`error`.

**Two things worth noting for the record (not new work, just read back):** the create step was explicitly no-post, so nothing here is published or attached; and the asset URLs above are already-public gateway paths, not new files.

*Left for the owner:* issue the one read-only `productions.get` / `productions.status` call for `14c25e77-225f-4cfc-9ede-8f4c7c515d77` and paste back the fields above; I will then fill effective durations, sound, spend, and whether the cut is video.
