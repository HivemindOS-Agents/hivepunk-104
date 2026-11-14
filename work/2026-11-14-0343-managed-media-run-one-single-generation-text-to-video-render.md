# Managed Media: run ONE single-generation text-to-video render, model minimax-h3-max-text-to-video, 15 seconds, 9:16 vertical, silent (no audio track at all), locked static camera, single continuous take. Set maxCredits to 2156 (the quoted amount). Prompt: "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds perfectly still the whole time. In one continuous take the worm first wiggles in place, then lifts a flipper to tip its black top hat toward the viewer, then wobbles side to side, spins once all the way around and bows low toward the camera, then finishes with a matching full spin and claps its flippers together. Silent, no audio."

**Failed**

2026-11-14 03:43 UTC, spent $0.01

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_b4d7c777e14ffadb40885c17ab78402d",
    "status": "queued",
    "title": "Worm dance, final — silent vertical",
    "shotCount": 1,
    "createdAt": "2026-11-14T03:43:03.829Z",
    "updatedAt": "2026-11-14T03:43:03.829Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, final — silent vertical",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds perfectly still the whole time. In one continuous take the worm first wiggles in place, then lifts a flipper to tip its black top hat toward the viewer, then wobbles side to side, spins once all the way around and bows low toward the camera, then finishes with a matching full spin and claps its flippers together. Silent, no audio.",
          "seconds": 15,
          "model": "minimax-h3-max-text-to-video"
        }
      ],
      "sound": {
        "mode": "silent"
      },
      "captions": [],
      "aspect": "9:16",
      "maxCredits": 2156,
      "keyframeModel": "gpt-image-2-image-to-image"
    },
    "quote": {
      "priceCredits": 2156,
      "maximumCredits": 2156,
      "priceUsd": 4.312,
      "expectedSeconds": 15.083,
      "items": [
        {
          "kind": "shot",
          "shotIndex": 0,
          "model": "minimax-h3-max-text-to-video",
          "priceUsd": 4.212,
          "maximumUsd": 4.212
        },
        {
          "kind": "assembly",
          "model": "studio-assembly",
          "priceUsd": 0.1,
          "maximumUsd": 0.1
        }
      ]
    },
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged."
  }
}
```
