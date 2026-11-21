# Read the finished result: In Hivemind Studio, quote and produce 'Worm dance, episode 7' — vertical 9:16, three 5-second text-mode shots on minimax-h3-max-text-to-video, each clip keeping its own model audio, no captions. Restate the character in every shot prompt: 'small bright red cartoon worm, big round white googly eyes with black pupils, shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, locked-off centred medium shot, clean vector cartoon look, absolutely no camera movement and no zoom.' Shot 1: the worm does a slow wobbly belly-slide sh

**Done**

2026-11-21 09:57 UTC, cost not known

- https://hivemindos.app/bee/104

```json
{
  "videoUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/ef01fa77-f611-49ba-9f13-8f2686818fa8.mp4",
  "posterUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/a804de52-3b32-4e1e-88a4-0ad2988c6feb.jpg",
  "durationSeconds": 15.6,
  "shots": [
    {
      "index": 0,
      "status": "complete",
      "durationSeconds": 5.167,
      "motion": {
        "mean": 7.89,
        "frozenSeconds": 0.25
      }
    },
    {
      "index": 1,
      "status": "complete",
      "durationSeconds": 5.167,
      "motion": {
        "mean": 21.85,
        "frozenSeconds": 0
      }
    },
    {
      "index": 2,
      "status": "complete",
      "durationSeconds": 5.167,
      "motion": {
        "mean": 17.32,
        "frozenSeconds": 0.5
      }
    }
  ],
  "qa": {
    "seams": [
      {
        "index": 1,
        "atSeconds": 5.167,
        "difference": 35.69,
        "kind": "pop"
      },
      {
        "index": 2,
        "atSeconds": 10.334,
        "difference": 34.95,
        "kind": "pop"
      }
    ],
    "audioPeak": 0.8414,
    "contactSheetUrl": "https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/a74bb10a-14ea-47d3-8e0b-1c1aed597df6.jpg"
  }
}
```
