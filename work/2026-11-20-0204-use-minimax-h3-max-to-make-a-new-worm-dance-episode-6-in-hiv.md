# Use MiniMax H3 Max to make a new worm dance episode 6 in Hivemind Studio: a vertical 9:16 video in 3 shots of about 5 seconds each, text mode, using the studio's own sound. Keep the character identical in every shot prompt: a small bright red cartoon worm with big round white googly eyes and black pupils, a shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint backdrop and floor, flat even lighting, locked-off camera at its eye level, clean vector cartoon look. Shot 1: the worm does a bouncy little tap-dance shuffle and tips its hat. Shot 2: it does a quick spin and then a hop, the hat staying on. Shot 3: it takes a bow and blows a kiss. Quote it first and keep the total under the 1500 credit cap, then create it, wait for the finished video, and report the video link and the QA seam check.

**Done**

2026-11-20 02:04 UTC, spent $0.00

Thought with claude-haiku-5-5, deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0045; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 9671.73
}
```
