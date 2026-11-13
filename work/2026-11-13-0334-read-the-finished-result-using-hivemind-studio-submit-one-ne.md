# Read the finished result: Using Hivemind Studio, submit one new production exactly matching the plan already quoted at $3.34 total (under the $9.89 ceiling): a three-shot vertical 9:16 video, text mode only with no picture links anywhere, model-generated sound, about 5 seconds per shot, same worm/mascot character in all three shots on a bright flat-color stage. Use these exact per-shot models and shot indexes so the price matches the quote: shotIndex 0 = kling-v3.0-pro-text-to-video ($1.08), shotIndex 1 = kling-v3.0-pro-text-to-video ($1.08), shotIndex 2 = kling-v3.0-pro-text-to-video ($1.08), plus studio-assembly at $

**Done**

2026-11-13 03:34 UTC, spent $0.00

- https://hivemindos.app/bee/104

```json
{
  "videoUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/c72561fd-2fe1-4457-8881-1bd7fe687674.mp4",
  "posterUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/3e19cef5-3883-4bb9-b576-150dd68c4fc2.jpg",
  "durationSeconds": 15.2,
  "shots": [
    {
      "index": 0,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/77b78bf5-2fa1-45c9-afc7-c2c77b980681.mp4",
      "durationSeconds": 5.042,
      "motion": {
        "mean": 14.27,
        "frozenSeconds": 0.25
      }
    },
    {
      "index": 1,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/c8b33c2a-990c-408a-a198-68ac22a047bf.mp4",
      "durationSeconds": 5.042,
      "motion": {
        "mean": 6.42,
        "frozenSeconds": 1
      }
    },
    {
      "index": 2,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/c3baec51-eda1-4823-9602-42e1893ca6ea.mp4",
      "durationSeconds": 5.042,
      "motion": {
        "mean": 13.51,
        "frozenSeconds": 1.25
      }
    }
  ],
  "qa": {
    "seams": [
      {
        "index": 1,
        "atSeconds": 5.042,
        "difference": 85.4,
        "kind": "cut"
      },
      {
        "index": 2,
        "atSeconds": 10.083,
        "difference": 23.91,
        "kind": "pop"
      }
    ],
    "audioPeak": 0.8414,
    "contactSheetUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/ed0d1971-3337-487b-a890-2453d3e7cc81.jpg"
  }
}
```
