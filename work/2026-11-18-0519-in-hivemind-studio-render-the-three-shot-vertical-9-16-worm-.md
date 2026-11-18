# In Hivemind Studio, render the three-shot vertical 9:16 worm dance video on MiniMax H3 Max with the video model's native sound kept ON (sound mode not silent, no separate audio step, no captions): shot 1 (~5s) a small red cartoon worm with big googly eyes in a black top hat on a bright flat-color stage, wiggling then tipping its hat; shot 2 (~5s) the same worm wobbling, one full spin and a bow; shot 3 (~5s) finishing with another full spin and a flipper clap; camera locked off, clean vector cartoon look. Set maxCredits to 2156, render it, and return the finished video link.

**Failed**

2026-11-18 05:19 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0097; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_dcbbe67cb1f6ee5fc566f4722f5e6dcd",
    "status": "queued",
    "title": "Worm dance — vertical, native sound",
    "shotCount": 3,
    "createdAt": "2026-11-18T05:19:50.998Z",
    "updatedAt": "2026-11-18T05:19:50.998Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance — vertical, native sound",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm with big round white googly eyes and black pupils, wearing a shiny black top hat set straight on its head, with two stubby flippers; on a bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. The worm wiggles in place, then lifts a flipper and tips its black top hat toward the viewer, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It wobbles side to side, spins one full turn all the way around and bows low toward the camera, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It finishes with one more full spin and claps its two flippers together, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        }
      ],
      "sound": {
        "mode": "model"
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
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged. A production that rendered every shot but failed before they were cut together keeps its clips: productions.finish makes the cut from them, so nothing is rendered or charged a second time."
  }
}
```
