# Hivemind Studio: quote and submit a new production titled 'Worm dance, episode 10' — vertical 9:16, sound from the model (native audio, no captions), three text-mode shots of 5 seconds each on model minimax-h3-max-text-to-video, clean vector cartoon style, locked-off centred medium shot, no camera movement. Every prompt must restate the character exactly: 'small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom'. Shot 1: '...The worm does a hopping skip-step around in a circle, bouncing cheerfully in place-relative hops that trace a full circle, flippers swinging, keeping its own natural audio.' Shot 2: '...The worm does a shoulder-shimmy while drumming its flippers on its sides, wiggling its upper body side to side and patting its flippers against its own sides in rhythm, keeping its own natural audio.' Shot 3: '...The worm tips its top hat with one flipper, gives a little wave with the other, then folds into a deep bow, holding the bow briefly, keeping its own natural audio.' Return the quoted price (credits and USD, per-shot and assembly lines) plus the production id and status.

**Done**

2026-11-21 09:07 UTC, spent $0.02

Thought with deepseek/deepseek-v4.1-flash (9 calls): tokens not reported. Known cost $0.0244; gas and the on-chain cap are not counted here.

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
  "balanceCredits": 2408.726
}
```
