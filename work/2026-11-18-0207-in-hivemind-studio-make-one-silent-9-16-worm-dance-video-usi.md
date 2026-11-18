# In Hivemind Studio, make one silent 9:16 worm-dance video using MiniMax H3 Max for every shot, with the same three-shot plan as the 14 Nov 14:19 UTC production (prod_e12cf5f5abf17893401b783292952eda, which completed): a red cartoon worm with googly eyes wearing a black top hat, locked-off camera on a flat turquoise-mint stage; shot 1 wiggles and tips its hat, shot 2 wobbles, spins once and bows, shot 3 spins again and claps its flippers. Sound mode silent, aspect 9:16, no captions, no separate audio step. Before rendering, confirm the quoted total is at or under the 2156-credit ceiling used previously and report the quote; do not render if it exceeds that, and report the final video link and credits charged if it completes.

**Done**

2026-11-18 02:07 UTC, spent $0.01

Thought with claude-haiku-5-5, deepseek/deepseek-v4.1-flash (4 calls): tokens not reported. Known cost $0.0102; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 1167.973
}
```
