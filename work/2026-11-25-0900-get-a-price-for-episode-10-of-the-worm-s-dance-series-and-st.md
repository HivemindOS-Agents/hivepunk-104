# Get a price for episode 10 of the worm's dance series and start making it: 3 shots, about 5 seconds each, vertical 9:16, using MiniMax H3 Max, text-to-video only, no reference picture. Same character in every shot: a small bright red cartoon worm with big round white googly eyes and black pupils, a shiny black top hat set straight on its head, and two stubby flippers, on a plain seamless turquoise-mint stage with flat even lighting, locked-off centred medium shot at its eye level, clean vector cartoon look, no camera movement. Shot 1: it does a clumsy hula-style hip wiggle with both flippers waving above its head. Shot 2: it hops forward in a little conga line of one, kicking one flipper out on each hop, wobbling. Shot 3: it stops, taps a flipper on the brim of its hat, then takes a big flustered bow to camera. Keep each clip's own model audio.

**Done**

2026-11-25 09:00 UTC, spent $0.02

Thought with deepseek/deepseek-v4.1-flash (2 calls): tokens not reported. Known cost $0.0151; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "quote": {
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
    "expectedSeconds": 15.501,
    "priceUsd": 0.44,
    "maximumUsd": 1.8,
    "priceCredits": 220,
    "maximumCredits": 900,
    "currency": "USD",
    "way": "rented",
    "minutes": 15,
    "otherWay": {
      "way": "fast",
      "priceUsd": 4.312,
      "maximumUsd": 4.312,
      "priceCredits": 2156,
      "maximumCredits": 2156,
      "minutes": 5
    },
    "rental": {
      "usdPerHour": 1.7,
      "gpu": "RTX 5090",
      "expectedMinutes": 12,
      "maximumMinutes": 51,
      "startBalanceUsd": 1.7
    },
    "maxCredits": 2500,
    "withinBudget": true
  },
  "balanceCredits": 647.21
}
```
