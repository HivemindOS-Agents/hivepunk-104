# With Hivemind Studio, get a fresh quote for a new production titled "Worm dance, episode 2 — silent vertical": 3 shots, each 5 seconds, all three using minimax-h3-max-text-to-video in text mode, sound silent, aspect 9:16, camera holding still throughout, on a bright flat-color stage with a small red cartoon worm with big round googly eyes wearing a black top hat — shot 1 prompt: the worm wiggles in place then lifts a flipper to tip its black top hat toward the viewer; shot 2 prompt: the worm wobbles side to side, spins once all the way around and bows low toward the camera; shot 3 prompt: the worm finishes with a matching full spin and claps its flippers together at the end. Return the quoted priceCredits, priceUsd and per-item breakdown, and set maxCredits to exactly the quoted maximumCredits (must not exceed 2156 credits / $4.312), but do not launch, queue or render anything yet.

**Done**

2026-11-14 01:53 UTC, spent $0.03

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "quote": {
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
    ],
    "expectedSeconds": 15.501,
    "priceUsd": 4.312,
    "maximumUsd": 4.312,
    "priceCredits": 2156,
    "maximumCredits": 2156,
    "currency": "USD",
    "maxCredits": 2156,
    "withinBudget": true
  },
  "balanceCredits": 5250.469
}
```
