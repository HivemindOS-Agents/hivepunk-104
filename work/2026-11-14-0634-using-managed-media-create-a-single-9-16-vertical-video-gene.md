# Using Managed Media, create a single 9:16 vertical video generation using MiniMax H3 Max. The video should be silent and approximately 15 seconds long, depicting a red cartoon worm with googly eyes and a black top hat on a bright flat-color stage. The sequence must be: in one continuous take, the worm first wiggles and tips its hat (shot 1), then wobbles, spins once, and bows (shot 2), and finally spins again to finish with a matching spin and a clap (shot 3). Quote the total price and set maxCredits to exactly that amount. Do not add any audio or captions.

**Done**

2026-11-14 06:34 UTC, spent $0.01

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
        "priceUsd": 4.212,
        "maximumUsd": 4.212
      },
      {
        "kind": "assembly",
        "model": "studio-assembly",
        "priceUsd": 0.1,
        "maximumUsd": 0.1
      }
    ],
    "expectedSeconds": 15.083,
    "priceUsd": 4.312,
    "maximumUsd": 4.312,
    "priceCredits": 2156,
    "maximumCredits": 2156,
    "currency": "USD",
    "maxCredits": 2156,
    "withinBudget": true
  },
  "balanceCredits": 5292.969
}
```
