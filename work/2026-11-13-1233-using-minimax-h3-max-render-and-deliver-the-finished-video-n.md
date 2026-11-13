# Using MiniMax H3 Max, render and deliver the finished video now — this run must produce the clip, not another price estimate. One silent vertical 9:16 video, about 15 seconds, made in a single text-to-video generation with no audio track: a bright flat-color stage with a red cartoon worm in a black top hat and googly eyes; beat 1 tips its hat (~5s), beat 2 wobbles, spins and bows (~5s), beat 3 finishes with a matching spin and clap (~5s). Spend up to $4.32, the amount already quoted and approved, and return the finished video link.

**Failed**

2026-11-13 12:33 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_8514f26fcdb150c285782ed1b6f2b065",
    "status": "queued",
    "title": "Worm dance, episode 1 — silent vertical",
    "shotCount": 3,
    "createdAt": "2026-11-13T12:33:18.692Z",
    "updatedAt": "2026-11-13T12:33:18.692Z",
    "finishedAt": null,
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
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
