# In Hivemind Studio, quote and produce 'Worm dance, episode 7' — vertical 9:16, three 5-second text-mode shots on minimax-h3-max-text-to-video, each clip keeping its own model audio, no captions. Restate the character in every shot prompt: 'small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom.' Shot 1: the worm does a slow wobbly belly-slide shimmy across the floor, rippling head to tail. Shot 2: the worm does a stiff sideways crab-step, flippers clicking like castanets. Shot 3: the worm does a wild double spin, tips its hat, then bows deep to the camera. Return the production id and status.

**Failed**

2026-11-21 09:47 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0139; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_de30ddeb27daa7d6d30a04f39776eafe",
    "status": "queued",
    "title": "Worm dance, episode 7",
    "shotCount": 3,
    "createdAt": "2026-11-21T09:47:15.656Z",
    "updatedAt": "2026-11-21T09:47:15.656Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 7",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm does a slow wobbly belly-slide shimmy across the floor, rippling head to tail, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-rented-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm does a stiff sideways crab-step, flippers clicking like castanets, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-rented-text-to-video"
        },
        {
          "mode": "text",
          "prompt": "small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom. The worm does a wild double spin, tips its hat, then bows deep to the camera, keeping its own natural audio.",
          "seconds": 5,
          "model": "minimax-h3-rented-text-to-video"
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
      "priceCredits": 220,
      "maximumCredits": 900,
      "priceUsd": 0.44,
      "expectedSeconds": 15.501,
      "items": [
        {
          "kind": "shot",
          "shotIndex": 0,
          "model": "minimax-h3-rented-text-to-video",
          "priceUsd": 0,
          "maximumUsd": 0
        },
        {
          "kind": "shot",
          "shotIndex": 1,
          "model": "minimax-h3-rented-text-to-video",
          "priceUsd": 0,
          "maximumUsd": 0
        },
        {
          "kind": "shot",
          "shotIndex": 2,
          "model": "minimax-h3-rented-text-to-video",
          "priceUsd": 0,
          "maximumUsd": 0
        },
        {
          "kind": "rental",
          "model": "rented-gpu",
          "priceUsd": 0.34,
          "maximumUsd": 1.7
        },
        {
          "kind": "assembly",
          "model": "studio-assembly",
          "priceUsd": 0.1,
          "maximumUsd": 0.1
        }
      ],
      "way": "rented",
      "minutes": 15,
      "rental": {
        "usdPerHour": 1.7,
        "gpu": "RTX 5090",
        "expectedMinutes": 12,
        "maximumMinutes": 51,
        "startBalanceUsd": 1.7
      }
    },
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged. A production that rendered every shot but failed before they were cut together keeps its clips: productions.finish makes the cut from them, so nothing is rendered or charged a second time. Shots made on a rented GPU are not charged by the clip: the machine is rented on your credits for the production, charged by the GPU rentals service for the minutes it ran (it holds ten minutes at a time and gives back what was not used; the quote's rental line is its expected and its most), and given back when its clips are made, when the production fails and when it is cancelled."
  }
}
```
