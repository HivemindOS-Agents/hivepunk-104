# Using Hivemind Studio, produce the three-shot vertical 9:16 silent worm dance video in ONE single MiniMax H3 Max text-to-video generation: shot 1 ~5s (red cartoon worm, black top hat, big googly eyes, bright flat-color stage, tips hat to viewer); shot 2 ~5s (wobbles side to side, spins once, bows); shot 3 ~5s (matching spin-and-clap finish); camera locked still, no captions, no audio, ~15s total. Quote the price first, set maxCredits to exactly the quoted amount, then poll to completion and return the finished video's shareable link and the actual dollars charged.

**Failed**

2026-11-14 06:51 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_c33e57a20a1af7094ce003d13093887a",
    "status": "queued",
    "title": "Worm Dance",
    "shotCount": 3,
    "createdAt": "2026-11-14T06:51:10.219Z",
    "updatedAt": "2026-11-14T06:51:10.219Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm Dance",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small red cartoon worm with big round googly eyes, wearing a black top hat, on a bright flat-color stage, evenly lit; the camera holds perfectly still as the worm wiggles in place, then lifts a flipper to tip its black top hat toward the viewer. Silent, no audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small red cartoon worm with big round googly eyes in a black top hat, on the same bright flat-color stage; it wobbles side to side, spins once all the way around and bows low toward the camera, camera holding still. Silent, no audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small red cartoon worm with big round googly eyes in a black top hat on the bright flat-color stage; it finishes with a matching full spin and claps its flippers together at the end, camera holding still. Silent, no audio.",
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
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
