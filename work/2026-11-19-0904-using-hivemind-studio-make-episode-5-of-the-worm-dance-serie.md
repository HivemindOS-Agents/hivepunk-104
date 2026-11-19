# Using Hivemind Studio, make episode 5 of the worm dance series, a 15-second vertical 9:16 video in 3 shots of 5 seconds each on minimax-h3-max-text-to-video. The worm's wobbly waltz: shot 1 the red cartoon worm in its black top hat sways left and right in a waltz rhythm on the same plain turquoise-mint flat stage, locked-off eye-level camera; shot 2 it twirls a full turn and dips low; shot 3 it spins back up and takes a bow. Describe the worm's full look in every shot prompt. Quote first, then create only if the quote is within 1500 credits.

**Done**

2026-11-19 09:04 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (4 calls): tokens not reported. Known cost $0.0120; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 1872.75
}
```
