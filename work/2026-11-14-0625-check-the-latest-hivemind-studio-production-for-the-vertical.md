# Check the latest Hivemind Studio production for the vertical silent worm dance clip (the one started from the single MiniMax H3 Max 15-second generation request): report whether it has finished rendering and been cut together, give the finished video's shareable link and its running time, and state the actual amount charged in dollars. Do not start a new generation or change the plan; if it failed, report the failure reason and whether the shot itself still rendered.

**Done**

2026-11-14 06:25 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_b4d7c777e14ffadb40885c17ab78402d",
    "status": "failed",
    "title": "Worm dance, final — silent vertical",
    "shotCount": 1,
    "createdAt": "2026-11-14T03:43:03.829Z",
    "updatedAt": "2026-11-14T03:51:30.027Z",
    "finishedAt": "2026-11-14T03:51:30.027Z",
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, final — silent vertical",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds perfectly still the whole time. In one continuous take the worm first wiggles in place, then lifts a flipper to tip its black top hat toward the viewer, then wobbles side to side, spins once all the way around and bows low toward the camera, then finishes with a matching full spin and claps its flippers together. Silent, no audio.",
          "seconds": 15,
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
      "expectedSeconds": 15.083,
      "items": [
        {
          "kind": "shot",
          "shotIndex": 0,
          "model": "minimax-h3-max-text-to-video",
          "priceUsd": 4.212,
          "maximumUsd": 4.212
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
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/7ba30fe7-73f4-4631-958a-1284271692e6.mp4"
      }
    ],
    "error": "The production stopped on an unexpected error. Finished shots are listed; nothing was charged for assembly.",
    "errorCode": "production_failed",
    "assemblyFee": "none",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
