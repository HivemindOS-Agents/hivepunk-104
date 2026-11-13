# With Hivemind Studio, check the current status of production prod_8514f26fcdb150c285782ed1b6f2b065 (title "Worm dance, episode 1 — silent vertical", shotCount 3, all three shots minimax-h3-max-text-to-video, sound silent, aspect 9:16, quote maximumCredits 2156 / $4.312, created 2026-11-13T12:33:18.692Z; this is the re-run that previously failed as prod_8514f26fcdb150c285782ed1b6f2b065) and return its latest state verbatim: status (queued/running/succeeded/failed/cancelled), updatedAt, finishedAt, cancelRequested, per-shot entries in the shots array with each shot's status, model and output, the assemblyFee state, and — if and only if it has finished and succeeded — the finished video link/URL, its duration and resolution/aspect, and confirmation that it is a silent vertical 9:16 clip of about 15 seconds. Do not launch, queue, re-quote or re-render anything in this step; read and report only.

**Done**

2026-11-13 13:53 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_8514f26fcdb150c285782ed1b6f2b065",
    "status": "failed",
    "title": "Worm dance, episode 1 — silent vertical",
    "shotCount": 3,
    "createdAt": "2026-11-13T12:33:18.692Z",
    "updatedAt": "2026-11-13T12:41:50.515Z",
    "finishedAt": "2026-11-13T12:41:50.515Z",
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 1 — silent vertical",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds still as the worm wiggles in place, then lifts a flipper to tip its black top hat toward the viewer.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small red cartoon worm with big round googly eyes in a black top hat, on the same bright flat-color stage; it wobbles side to side, spins once all the way around and bows low toward the camera, camera holding still.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small red cartoon worm with big round googly eyes in a black top hat on the bright flat-color stage; it finishes with a matching full spin and claps its flippers together at the end, camera holding still.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        }
      ],
      "sound": {
        "mode": "silent"
      },
      "captions": [],
      "aspect": "9:16",
      "maxCredits": 2156,
      "keyframeModel": "gpt-image-2-image-to-image"
    },
    "quote": {
      "priceCredits": 2156,
      "maximumCredits": 2156,
      "priceUsd": 4.312,
      "expectedSeconds": 15.501,
      "items": [
        {
          "kind": "shot",
          "shotIndex": 0,
          "model": "minimax-h3-max-text-to-video",
          "priceUsd": 1.404,
          "maximumUsd": 1.404
        },
        {
          "kind": "shot",
          "shotIndex": 1,
          "model": "minimax-h3-max-text-to-video",
          "priceUsd": 1.404,
          "maximumUsd": 1.404
        },
        {
          "kind": "shot",
          "shotIndex": 2,
          "model": "minimax-h3-max-text-to-video",
          "priceUsd": 1.404,
          "maximumUsd": 1.404
        },
        {
          "kind": "assembly",
          "model": "studio-assembly",
          "priceUsd": 0.1,
          "maximumUsd": 0.1
        }
      ]
    },
    "shots": [
      {
        "index": 0,
        "status": "complete",
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/0daec684-a9bd-466e-ad2a-0d4dd032e2f0.mp4"
      },
      {
        "index": 1,
        "status": "complete",
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/c3d3db1f-ba7c-47fb-a486-5e92f565fc3f.mp4"
      },
      {
        "index": 2,
        "status": "complete",
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/65d48412-23da-428f-9f6b-7b3fcbea854d.mp4"
      }
    ],
    "error": "The production stopped on an unexpected error. Finished shots are listed; nothing was charged for assembly.",
    "errorCode": "production_failed",
    "assemblyFee": "none",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
