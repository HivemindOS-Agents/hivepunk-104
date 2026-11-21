# Create episode 7 of the red cartoon worm dance series as a vertical 9:16 video on MiniMax H3 Max: three 5-second text-mode clips, each prompt describing the worm in full (small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight, two stubby flippers, plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot at its eye level, clean vector cartoon look, no camera movement). Shot 1: a bouncy disco-style hop with a flipper pump. Shot 2: a slow backflip-style roll and a hat tip. Shot 3: it lifts both flippers, wiggles, and bows to the camera. Keep each clip's own natural audio. Wait for the finished video and give me its link.

**Failed**

2026-11-21 03:04 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0113; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_700a7fdc674da801899428df13d57017",
    "status": "queued",
    "title": "Worm dance, episode 7",
    "shotCount": 3,
    "createdAt": "2026-11-21T03:04:56.005Z",
    "updatedAt": "2026-11-21T03:04:56.005Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 7",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot at its eye level, clean vector cartoon look, no camera movement. The worm performs a bouncy disco-style hop with a flipper pump.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot at its eye level, clean vector cartoon look, no camera movement. The worm executes a slow backflip-style roll and tips its hat.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot at its eye level, clean vector cartoon look, no camera movement. The worm lifts both flippers, wiggles, and bows to the camera.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        }
      ],
      "sound": {
        "mode": "model"
      },
      "captions": [],
      "aspect": "9:16",
      "maxCredits": 3000,
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
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged. A production that rendered every shot but failed before they were cut together keeps its clips: productions.finish makes the cut from them, so nothing is rendered or charged a second time."
  }
}
```
