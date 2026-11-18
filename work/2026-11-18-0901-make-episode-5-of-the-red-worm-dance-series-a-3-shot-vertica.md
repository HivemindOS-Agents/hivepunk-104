# Make episode 5 of the red-worm dance series: a 3-shot vertical 9:16 video, about 16 seconds, on MiniMax H3 Max, native clip audio. Character in every shot: a small bright red cartoon worm with big round white googly eyes and black pupils, a shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint flat-colour stage, even flat lighting, camera locked off at its eye level, clean vector cartoon look. Episode 5 is the worm's wobbly waltz: shot 1, it sways in 3/4 time and doffs its hat; shot 2, it pirouettes and almost topples, catching itself; shot 3, it takes a bow, hat over its chest. Quote first, then produce only if the quote is at or under 1500 credits and the studio balance covers it.

**Done**

2026-11-18 09:01 UTC, spent $0.02

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0169; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 445.602
}
```
