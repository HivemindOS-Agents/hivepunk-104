# Create episode 9 of the red cartoon worm dance series in Hivemind Studio: vertical 9:16, three 5-second text clips on MiniMax H3 Max, each keeping its own audio. Restate the character in every prompt: small bright red cartoon worm, white googly eyes, black top hat set straight, two stubby flippers, plain turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, no camera movement. Shots: a slow backwards moonwalk glide; a limbo-style lean-back; a quick cha-cha ending in a frozen pose. Quote first, then wait for the finished link.

**Failed**

2026-11-21 03:19 UTC, spent $0.02

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0151; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_e6c290c5f768f596ee93856a2b93548a",
    "status": "queued",
    "title": "Worm dance, episode 9",
    "shotCount": 3,
    "createdAt": "2026-11-21T03:19:41.994Z",
    "updatedAt": "2026-11-21T03:19:41.994Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 9",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm performs a slow backwards moonwalk glide, sliding smoothly backward across the stage with its flippers, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm does a limbo-style lean-back, arching backward low and holding the lean without falling, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm dances a quick cha-cha, stepping briskly side to side with its flippers, then snaps into a frozen final pose and holds it perfectly still, keeping its own natural audio.",
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
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged. A production that rendered every shot but failed before they were cut together keeps its clips: productions.finish makes the cut from them, so nothing is rendered or charged a second time. Shots made on a rented GPU are not charged by the clip: the machine is rented on your credits for the production, charged by the GPU rentals service for the minutes it ran in ten-minute blocks (the quote's rental line is its expected and its most), and given back when its clips are made, when the production fails and when it is cancelled."
  }
}
```
