# Produce episode 5 of the red-worm dance series ("wobbly waltz"): a 3-shot vertical 9:16 video on MiniMax H3 Max with each clip's native audio, ~16s. Character in every shot: a small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight, two stubby flippers, on a plain seamless turquoise-mint flat-colour stage, even flat lighting, camera locked off at its eye level, clean vector cartoon look, movement already underway from frame one. Shot 1: sways in 3/4 time and doffs its hat. Shot 2: pirouettes and almost topples, catching itself. Shot 3: takes a bow, hat over its chest. Quote first; produce only if the quote is at or under 1500 credits and the balance covers it.

**Done**

2026-11-19 03:07 UTC, spent $0.02

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0192; gas and the on-chain cap are not counted here.

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
    "maxCredits": 1500,
    "withinBudget": false
  },
  "balanceCredits": 902.392
}
```
