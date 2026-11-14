# With Hivemind Studio, retry the production titled "Worm dance, episode 2 — silent vertical" (id prod_e6b254b7b0fd22e793220ad9c1ee9d4e) that failed: 3 shots of 5 seconds each on minimax-h3-max-text-to-video in text mode, silent, 9:16, camera still throughout, on a bright flat-color stage with a small red cartoon worm with big round googly eyes wearing a black top hat — shot 1: wiggles in place then tips the hat toward the viewer; shot 2: wobbles, spins once and bows; shot 3: matching spin and claps flippers. Set maxCredits to 2156 and deliver the finished clip.

**Failed**

2026-11-14 02:09 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_04b7bbf97935788fa653c1e3cfa5c9f0",
    "status": "queued",
    "title": "Worm dance, episode 2 — silent vertical",
    "shotCount": 3,
    "createdAt": "2026-11-14T02:09:14.585Z",
    "updatedAt": "2026-11-14T02:09:14.585Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 2 — silent vertical",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds still as the worm wiggles in place, then lifts a flipper to tip its black top hat toward the viewer. Silent, no audio.",
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
