# Hivemind Studio: quote and submit production 'Worm dance, episode 11' — vertical 9:16, three 5-second text-mode shots on minimax-h3-max-text-to-video, sound from each clip's own model audio, no captions. Every prompt restates the character exactly: 'small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom'. Shot 1: the worm does a samba-style hip sway, rolling side to side with flippers held high. Shot 2: the worm does a clumsy one-flipper handstand wobble, teetering but staying up. Shot 3: the worm does a rapid tap-dance flurry of little steps, then freezes in a proud pose. Return the quoted price and production id/status.

**Done**

2026-11-21 09:10 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0133; gas and the on-chain cap are not counted here.

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
    "way": "fast",
    "minutes": 5,
    "otherWay": {
      "way": "rented",
      "priceUsd": 0.44,
      "maximumUsd": 1.8,
      "priceCredits": 220,
      "maximumCredits": 900,
      "minutes": 15
    },
    "maxCredits": 2500,
    "withinBudget": true
  },
  "balanceCredits": 2402.063
}
```
