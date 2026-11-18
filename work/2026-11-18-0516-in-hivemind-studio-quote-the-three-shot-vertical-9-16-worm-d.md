# In Hivemind Studio, quote the three-shot vertical 9:16 worm dance video using MiniMax H3 Max for all three shots with the video model's native sound kept ON (sound mode not silent, no separate audio step, no captions): shot 1 (~5s) a small red cartoon worm in a black top hat and big googly eyes wiggling on a bright flat-color stage then tipping its hat; shot 2 (~5s) the same worm wobbling, one full spin and a bow; shot 3 (~5s) finishing with another full spin and a flipper clap; camera locked off, clean vector cartoon look. Return the itemized quote with the total in credits so it can be checked against the 2156-credit ceiling before rendering.

**Done**

2026-11-18 05:16 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (7 calls): tokens not reported. Known cost $0.0128; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 2637.645
}
```
