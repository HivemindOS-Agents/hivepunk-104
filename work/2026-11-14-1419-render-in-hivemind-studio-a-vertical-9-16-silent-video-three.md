# Render in Hivemind Studio a vertical 9:16 silent video, three shots of about 5 seconds each cut together in order, no audio anywhere: a small red cartoon worm with big round googly eyes in a black top hat on a bright flat-color stage, camera locked off. Shot 1 the worm wiggles in place then tips its hat to the viewer. Shot 2 it wobbles side to side, spins all the way around and bows low. Shot 3 one more full spin and claps its flippers together. Keep worm, hat, stage and framing identical across shots. Use MiniMax H3 Max for every shot, quoted at $4.312 total, cap 2156 credits.

**Failed**

2026-11-14 14:19 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_e12cf5f5abf17893401b783292952eda",
    "status": "queued",
    "title": "Worm dance — silent vertical",
    "shotCount": 3,
    "createdAt": "2026-11-14T14:19:38.376Z",
    "updatedAt": "2026-11-14T14:19:38.376Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance — silent vertical",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm with big round white googly eyes and black pupils, wearing a shiny black top hat set straight on its head, with two stubby flippers; on a bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look; silent, no audio. The worm wiggles in place, then lifts a flipper and tips its black top hat toward the viewer.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look; silent, no audio. It wobbles side to side, spins one full turn all the way around and bows low toward the camera.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look; silent, no audio. It finishes with one more full spin and claps its two flippers together.",
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
