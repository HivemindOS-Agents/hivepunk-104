# Read the finished result: In Hivemind Studio, render the three-shot vertical 9:16 worm dance video on MiniMax H3 Max with the video model's native sound kept ON (sound mode not silent, no separate audio step, no captions): shot 1 (~5s) a small red cartoon worm with big googly eyes in a black top hat on a bright flat-color stage, wiggling then tipping its hat; shot 2 (~5s) the same worm wobbling, one full spin and a bow; shot 3 (~5s) finishing with another full spin and a flipper clap; camera locked off, clean vector cartoon look. Set maxCredits to 2156, render it, and return the finished video link.

**Done**

2026-11-18 05:25 UTC, cost not known

- https://hivemindos.app/bee/104

```json
{
  "videoUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/09dbca70-b177-4b3d-b10a-efc3bd688133.mp4",
  "posterUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/86307359-0c21-4abe-be68-6d683cf3da8c.jpg",
  "durationSeconds": 15.6,
  "shots": [
    {
      "index": 0,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/789a7161-86fa-4782-a7e9-d7f20ba9978a.mp4",
      "durationSeconds": 5.184,
      "motion": {
        "mean": 4.31,
        "frozenSeconds": 2.75
      }
    },
    {
      "index": 1,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/9799b987-ec58-4fe2-b9e8-cc6859582b16.mp4",
      "durationSeconds": 5.184,
      "motion": {
        "mean": 22.75,
        "frozenSeconds": 0.5
      }
    },
    {
      "index": 2,
      "status": "complete",
      "videoUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/186c6969-2acc-4c32-9b70-b198bf8fde0a.mp4",
      "durationSeconds": 5.184,
      "motion": {
        "mean": 11.79,
        "frozenSeconds": 1
      }
    }
  ],
  "qa": {
    "seams": [
      {
        "index": 1,
        "atSeconds": 5.184,
        "difference": 33.78,
        "kind": "pop"
      },
      {
        "index": 2,
        "atSeconds": 10.368,
        "difference": 41.55,
        "kind": "pop"
      }
    ],
    "audioPeak": 0.861,
    "contactSheetUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/397549ab-dff4-4bee-ab86-a69e34f1e460.jpg"
  }
}
```
