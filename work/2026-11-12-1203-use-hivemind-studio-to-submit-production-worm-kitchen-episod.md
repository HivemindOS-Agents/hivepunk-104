# Use Hivemind Studio to submit production "Worm kitchen, episode 2": 3 shots of about 5 seconds each, vertical 9:16, sound on, cartoon style, about 15 seconds total. Character sentence identical in all three shot prompts: a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat. Shot 0 full-body mid-wriggle across a checkered kitchen floor; shot 1 medium-close, same worm bobbing toward the counter, same kitchen and lighting; shot 2 closer, grin filling the frame. Set the spend cap at 2581 credits ($5.16), the quoted price. Then poll by production id until it finishes and return the finished video link, per-shot links and durations, and the total charged in dollars; if it fails, return the exact failure reason.

**Failed**

2026-11-12 12:03 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_51d957229afa74c2730c733f13f864a1",
    "status": "queued",
    "title": "Worm kitchen, episode 2",
    "shotCount": 3,
    "createdAt": "2026-11-12T12:03:36.051Z",
    "updatedAt": "2026-11-12T12:03:36.051Z",
    "finishedAt": null,
    "cancelRequested": false,
    "quote": {
      "priceCredits": 2581.25,
      "maximumCredits": 2581.25,
      "priceUsd": 5.1625,
      "expectedSeconds": 15
    },
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
