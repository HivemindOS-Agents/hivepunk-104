# Using Hivemind Studio, re-run the Episode 2 cartoon video job as a new job: 3 shots, vertical (9:16), sound on, target duration ~15 seconds (~5.042s per shot), based on the prior Episode 2 cartoon recreation. Authorized spend is exactly 1670 credits ($3.34 at 500 credits = $1.00), no more; the quote must be confirmed at or below that ceiling before rendering. Return the finished .mp4 link, the poster and contact sheet links, the actual duration in seconds, the audioPeak value from the result panel, and the settled charge in both credits and USD. If the quote exceeds 1670 credits, do not render and report the quote instead.

**Done**

2026-11-12 09:09 UTC, spent $0.03

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "quote": {
    "items": [
      {
        "kind": "shot",
        "shotIndex": 0,
        "model": "kling-v3.0-pro-text-to-video",
        "priceUsd": 1.08,
        "maximumUsd": 1.08
      },
      {
        "kind": "shot",
        "shotIndex": 1,
        "model": "kling-v3.0-pro-text-to-video",
        "priceUsd": 1.08,
        "maximumUsd": 1.08
      },
      {
        "kind": "shot",
        "shotIndex": 2,
        "model": "kling-v3.0-pro-text-to-video",
        "priceUsd": 1.08,
        "maximumUsd": 1.08
      },
      {
        "kind": "assembly",
        "model": "studio-assembly",
        "priceUsd": 0.1,
        "maximumUsd": 0.1
      }
    ],
    "expectedSeconds": 15,
    "priceUsd": 3.34,
    "maximumUsd": 3.34,
    "priceCredits": 1670,
    "maximumCredits": 1670,
    "currency": "USD",
    "maxCredits": 1670,
    "withinBudget": true
  },
  "balanceCredits": 1630.085
}
```
