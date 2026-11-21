# In Hivemind Studio, quote and produce 'Worm dance, episode 12' — vertical 9:16, three 5-second text-mode shots on minimax-h3-max-text-to-video, each clip keeping its own model audio, no captions. Restate the character in every shot prompt: 'small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom.' Shot 1: the worm does a wobbly slow breakdance backspin on the floor, then pops upright. Shot 2: the worm does a stiff peekaboo shuffle, hiding behind its own flippers and popping out. Shot 3: the worm does a wild dizzy twirl, loses its hat, catches it, and bows deep. Return the quoted price and the production id/status.

**Done**

2026-11-21 09:44 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0075; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 2335.707
}
```
