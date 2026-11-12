# Use Hivemind Studio to submit the Episode 2 cartoon re-run as production "Worm kitchen, episode 2": 3 shots of about 5 seconds each, vertical 9:16, sound on, cartoon style, total about 15 seconds, with the character sentence identical in all three shot prompts (a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat). Open shot 0 full-body mid-wriggle across a checkered kitchen floor; shot 1 medium-close, same worm bobbing toward the counter, same kitchen and lighting direction; shot 2 closer, same worm finishing the bit with the grin filling the frame. Set the spend cap at 1670 and stop if the quote exceeds it. Return the production id and quoted credits.

**Done**

2026-11-12 11:57 UTC, spent $0.02

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "quote": {
    "items": [
      {
        "kind": "shot",
        "shotIndex": 0,
        "model": "seedance-2-text-to-video",
        "priceUsd": 1.6875,
        "maximumUsd": 1.6875
      },
      {
        "kind": "shot",
        "shotIndex": 1,
        "model": "seedance-2-text-to-video",
        "priceUsd": 1.6875,
        "maximumUsd": 1.6875
      },
      {
        "kind": "shot",
        "shotIndex": 2,
        "model": "seedance-2-text-to-video",
        "priceUsd": 1.6875,
        "maximumUsd": 1.6875
      },
      {
        "kind": "assembly",
        "model": "studio-assembly",
        "priceUsd": 0.1,
        "maximumUsd": 0.1
      }
    ],
    "expectedSeconds": 15,
    "priceUsd": 5.1625,
    "maximumUsd": 5.1625,
    "priceCredits": 2581.25,
    "maximumCredits": 2581.25,
    "currency": "USD",
    "maxCredits": 1670,
    "withinBudget": false
  },
  "balanceCredits": 2451.356
}
```
