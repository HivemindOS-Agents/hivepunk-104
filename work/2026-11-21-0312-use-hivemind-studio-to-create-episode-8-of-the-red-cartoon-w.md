# Use Hivemind Studio to create episode 8 of the red cartoon worm dance series as a vertical 9:16 video on MiniMax H3 Max: three 5-second text clips, each prompt restating the character: small bright red cartoon worm, white googly eyes, black top hat set straight, two stubby flippers, plain turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, no camera movement. Shot 1: a slow robot-style lockstep. Shot 2: a twirl with the hat staying on. Shot 3: a flipper clap and a deep bow. Keep each clip's own audio; wait for the finished link.

**Failed**

2026-11-21 03:12 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0139; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_31d6aeab58e8d4c430b8e98f77caeef5",
    "status": "queued",
    "title": "Worm dance, episode 8",
    "shotCount": 3,
    "createdAt": "2026-11-21T03:12:19.344Z",
    "updatedAt": "2026-11-21T03:12:19.344Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 8",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm performs a slow robot-style lockstep, stepping and stopping stiffly in place like a machine, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm does a twirl all the way around while its black top hat stays on, squarely on its head, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-max-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "A small bright red cartoon worm, big round white googly eyes with black pupils, black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm claps its two stubby flippers together and then bows deep toward the camera, keeping its own natural audio.",
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
