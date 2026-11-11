# Use Hivemind Studio's read-only status check on production prod_f631e03b7895d1d5585187f531133e28 to confirm the finished video link https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/9e3755e1-700a-41a8-8ccc-43b5f573952e.mp4 and the three shot links are still live, and to fetch the total cost spent against the 1400-credit maxCredits budget. Do not start any new generation or spend credits; return the video link, poster link https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/bcb2720b-ee3b-4565-bde9-bf5277d98f40.jpg, shot count (3), duration (15.125 s), and the cost summary.

**Done**

2026-11-11 03:36 UTC, spent $0.00

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_f631e03b7895d1d5585187f531133e28",
    "status": "complete",
    "title": "Worm Disco Limbo Redux",
    "shotCount": 3,
    "createdAt": "2026-11-10T09:40:43.758Z",
    "updatedAt": "2026-11-10T09:46:41.404Z",
    "finishedAt": "2026-11-10T09:46:41.404Z",
    "cancelRequested": false,
    "quote": {
      "priceCredits": 1163.75,
      "maximumCredits": 1163.75,
      "priceUsd": 2.3275,
      "expectedSeconds": 15
    },
    "shots": [
      {
        "index": 0,
        "status": "complete",
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/043c8cc9-8648-43c5-b90f-a52acfa80b68.mp4",
        "durationSeconds": 5.042,
        "motion": {
          "mean": 7.19,
          "frozenSeconds": 4.75
        }
      },
      {
        "index": 1,
        "status": "complete",
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/e7e83945-b76d-4ce0-8e36-dea6b692363e.mp4",
        "durationSeconds": 5.042,
        "motion": {
          "mean": 12.48,
          "frozenSeconds": 0.5
        }
      },
      {
        "index": 2,
        "status": "complete",
        "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/c70f3809-2560-4ccd-8420-540858d3ada7.mp4",
        "durationSeconds": 5.042,
        "motion": {
          "mean": 8.57,
          "frozenSeconds": 1.75
        }
      }
    ],
    "result": {
      "videoUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/9e3755e1-700a-41a8-8ccc-43b5f573952e.mp4",
      "posterUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/bcb2720b-ee3b-4565-bde9-bf5277d98f40.jpg",
      "durationSeconds": 15.125,
      "shots": [
        {
          "index": 0,
          "status": "complete",
          "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/043c8cc9-8648-43c5-b90f-a52acfa80b68.mp4",
          "durationSeconds": 5.042,
          "motion": {
            "mean": 7.19,
            "frozenSeconds": 4.75
          }
        },
        {
          "index": 1,
          "status": "complete",
          "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/e7e83945-b76d-4ce0-8e36-dea6b692363e.mp4",
          "durationSeconds": 5.042,
          "motion": {
            "mean": 12.48,
            "frozenSeconds": 0.5
          }
        },
        {
          "index": 2,
          "status": "complete",
          "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/c70f3809-2560-4ccd-8420-540858d3ada7.mp4",
          "durationSeconds": 5.042,
          "motion": {
            "mean": 8.57,
            "frozenSeconds": 1.75
          }
        }
      ],
      "qa": {
        "seams": [
          {
            "index": 1,
            "atSeconds": 5.042,
            "difference": 97.05,
            "kind": "cut"
          },
          {
            "index": 2,
            "atSeconds": 10.083,
            "difference": 79.72,
            "kind": "cut"
          }
        ],
        "audioPeak": null,
        "contactSheetUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/c8fff99c-4cce-4086-a704-c9399346c3a0.jpg"
      }
    },
    "assemblyFee": "settled",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
