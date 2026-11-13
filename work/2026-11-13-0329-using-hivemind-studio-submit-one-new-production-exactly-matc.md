# Using Hivemind Studio, submit one new production exactly matching the plan already quoted at $3.34 total (under the $9.89 ceiling): a three-shot vertical 9:16 video, text mode only with no picture links anywhere, model-generated sound, about 5 seconds per shot, same worm/mascot character in all three shots on a bright flat-color stage. Use these exact per-shot models and shot indexes so the price matches the quote: shotIndex 0 = kling-v3.0-pro-text-to-video ($1.08), shotIndex 1 = kling-v3.0-pro-text-to-video ($1.08), shotIndex 2 = kling-v3.0-pro-text-to-video ($1.08), plus studio-assembly at $0.10, expectedSeconds 15, priceCredits 1670. Shot 1 (shotIndex 0, prompt): same worm/mascot character, bright flat-color stage, the character tips its hat. Shot 2 (shotIndex 1): the same worm/mascot character on the same bright flat-color stage spins with a wobble, then bows. Shot 3 (shotIndex 2): the same worm/mascot character on the same bright flat-color stage waves cheerfully. No reference pictures or image URLs in any field — model text prompts only. Do not retry if rejected. Return verbatim: the production id (if any), the exact status the submit call returns, the exact error text, and any per-shot error text; if the submit is rejected (for example on credits or API schema), return the verbatim rejection reason and nothing else.

**Failed**

2026-11-13 03:29 UTC, spent $0.02

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_5a46ce0d37de53519fb6eddf5378c0e7",
    "status": "queued",
    "title": "Worm mascot, three shots",
    "shotCount": 3,
    "createdAt": "2026-11-13T03:29:38.890Z",
    "updatedAt": "2026-11-13T03:29:38.890Z",
    "finishedAt": null,
    "cancelRequested": false,
    "quote": {
      "priceCredits": 1670,
      "maximumCredits": 1670,
      "priceUsd": 3.34,
      "expectedSeconds": 15
    },
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
