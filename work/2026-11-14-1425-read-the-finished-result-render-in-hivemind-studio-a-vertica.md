# Read the finished result: Render in Hivemind Studio a vertical 9:16 silent video, three shots of about 5 seconds each cut together in order, no audio anywhere: a small red cartoon worm with big round googly eyes in a black top hat on a bright flat-color stage, camera locked off. Shot 1 the worm wiggles in place then tips its hat to the viewer. Shot 2 it wobbles side to side, spins all the way around and bows low. Shot 3 one more full spin and claps its flippers together. Keep worm, hat, stage and framing identical across shots. Use MiniMax H3 Max for every shot, quoted at $4.312 total, cap 2156 credits.

**Done**

2026-11-14 14:25 UTC, spent $0.00

- https://hivemindos.app/bee/104

```json
{
  "videoUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/7c5991c1-6a8b-494e-bcbf-b421bc00fff1.mp4",
  "posterUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/60646843-b030-42f5-9b90-6506d6fbefe4.jpg",
  "durationSeconds": 15.552,
  "shots": [
    {
      "index": 0,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/2790a877-6dc7-4ab9-bd23-e4908513bff3.mp4",
      "durationSeconds": 5.184,
      "motion": {
        "mean": 4.1,
        "frozenSeconds": 1.75
      }
    },
    {
      "index": 1,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/f6ee6ed9-3b4f-47f2-998b-9751d7a4dcf7.mp4",
      "durationSeconds": 5.184,
      "motion": {
        "mean": 16.75,
        "frozenSeconds": 0.5
      }
    },
    {
      "index": 2,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/a324413f-cf45-461e-ab9d-f2bb0b10538d.mp4",
      "durationSeconds": 5.184,
      "motion": {
        "mean": 13.75,
        "frozenSeconds": 1
      }
    }
  ],
  "qa": {
    "seams": [
      {
        "index": 1,
        "atSeconds": 5.184,
        "difference": 28.65,
        "kind": "pop"
      },
      {
        "index": 2,
        "atSeconds": 10.368,
        "difference": 41.01,
        "kind": "pop"
      }
    ],
    "audioPeak": null,
    "contactSheetUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/dd9cae42-1185-4d32-947a-cd4c7c3018ae.jpg"
  }
}
```
