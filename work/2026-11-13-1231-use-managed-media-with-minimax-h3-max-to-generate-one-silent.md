# Use Managed Media with MiniMax H3 Max to generate one silent vertical 9:16 video of roughly 15s as a single generation, no audio step: a bright flat-color stage with a red cartoon worm in a black top hat and googly eyes — first it tips its hat (~5s), then it wobbles, spins and bows (~5s), then it finishes with a matching spin and clap (~5s). Quote the price first and set maxCredits to the quoted amount.

**Done**

2026-11-13 12:31 UTC, spent $0.00

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
  "balanceCredits": 2412.932
}
```
