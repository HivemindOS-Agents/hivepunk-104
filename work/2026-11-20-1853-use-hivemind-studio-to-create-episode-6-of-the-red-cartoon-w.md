# Use Hivemind Studio to create episode 6 of the red cartoon worm dance series as a vertical 9:16 video: three 5-second text-mode clips on MiniMax H3 Max, each prompt describing the worm in full (small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight, two stubby flippers, plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot at its eye level, clean vector cartoon look, no camera movement). Shot 1: a moonwalk-style sliding glide across the stage. Shot 2: a flipper-flap shimmy with shoulders wobbling. Shot 3: it tosses its top hat up, spins, and catches it back on its head with a bow. Keep each clip's own natural audio. Then wait for the finished video and give me its link.

**Failed**

2026-11-20 18:53 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0058; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_9e6f7d0a656a83b0cb31e74dda37847c",
    "status": "queued",
    "title": "Worm dance, episode 6 — vertical, native sound",
    "shotCount": 3,
    "createdAt": "2026-11-20T18:53:14.768Z",
    "updatedAt": "2026-11-20T18:53:14.768Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 6 — vertical, native sound",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm with big round white googly eyes and black pupils, wearing a shiny black top hat set straight on its head, with two stubby flippers; on a bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; flat even lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It slides across the stage in a smooth moonwalk-style glide, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; flat even lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It does a flipper-flap shimmy, flapping both stubby flippers while its shoulders wobble side to side, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; flat even lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It tosses its black top hat up in the air, spins once, and catches the hat back on its head, then bows to the camera, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        }
      ],
      "sound": {
        "mode": "model"
      },
      "captions": [],
      "aspect": "9:16",
      "maxCredits": 2500,
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
