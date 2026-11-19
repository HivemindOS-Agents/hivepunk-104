# Make episode 5 of the worm dance series: a vertical 9:16 video, 3 shots of about 5 seconds each with MiniMax H3 Max in text mode, using the studio's own sound. Keep the character identical in every shot prompt: a small bright red cartoon worm with big round white googly eyes and black pupils, a shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint backdrop and floor, flat even lighting, locked-off camera at its eye level, clean vector cartoon look. Shot 1: the worm tries a wobbly waltz, swaying off balance and tipping its hat. Shot 2: it spins, its top hat tilts, then it wobbles upright again with a little shrug. Shot 3: it bows, then claps its flippers and hops once. Quote it first, then create it and wait for the finished video, and give me the video link.

**Failed**

2026-11-19 15:38 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0082; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_a3cbd10838086c1157d37ef459c81a01",
    "status": "queued",
    "title": "Worm dance, episode 5 — vertical, native sound",
    "shotCount": 3,
    "createdAt": "2026-11-19T15:38:24.091Z",
    "updatedAt": "2026-11-19T15:38:24.091Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 5 — vertical, native sound",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm with big round white googly eyes and black pupils, wearing a shiny black top hat set straight on its head, with two stubby flippers; on a bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; flat even lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. The worm tries a wobbly waltz, swaying off balance left and right in waltz rhythm and tipping its black top hat toward the viewer, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; flat even lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It spins, its black top hat tilts sideways, then it wobbles upright again with a little shrug, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "The same small bright red cartoon worm with big round white googly eyes and black pupils, wearing the same shiny black top hat set straight on its head, with two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; flat even lighting with no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, identical centred medium shot, vertical 9:16, absolutely no camera movement and no zoom; clean vector cartoon look. It bows toward the camera, then claps its two stubby flippers together and hops once, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        }
      ],
      "sound": {
        "mode": "model"
      },
      "captions": [],
      "aspect": "9:16",
      "maxCredits": 2160,
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
