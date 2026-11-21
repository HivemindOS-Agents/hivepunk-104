# Quote and produce 'Worm dance, episode 7' using MiniMax H3 Max, consisting of three 5-second vertical 9:16 shots.

**Done**

2026-11-21 09:00 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0103; gas and the on-chain cap are not counted here.

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
    "way": "fast",
    "minutes": 5,
    "otherWay": {
      "way": "rented",
      "priceUsd": 0.44,
      "maximumUsd": 1.8,
      "priceCredits": 220,
      "maximumCredits": 900,
      "minutes": 15
    },
    "maxCredits": 2500,
    "withinBudget": true
  },
  "balanceCredits": 926.492
}
```
