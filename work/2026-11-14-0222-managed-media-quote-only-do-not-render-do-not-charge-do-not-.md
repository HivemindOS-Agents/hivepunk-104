# Managed Media: quote only — do not render, do not charge, do not create the video yet. Return the exact price for one single-generation text-to-video render with these fixed parameters: model minimax-h3-max-text-to-video, mode text-to-video, one continuous take (single generation, no shot splitting, no keyframes, no assembly), duration roughly 15 seconds, aspect ratio 9:16 vertical, silent (no audio, no music, no voiceover, no sound effects), camera locked/static throughout with no camera movement. Prompt to price exactly as written: "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds perfectly still the whole time. In one continuous take the worm first tips its black top hat toward the viewer, then wobbles and spins once all the way around and bows low toward the camera, then finishes with a matching full spin and claps its flippers together. Silent, no audio." Reply with: priceCredits, maximumCredits, priceUsd, and every line item (model, kind, seconds, price) that makes up the total, so I can compare the total USD against a hard owner limit of $4.32 before authorizing the render. Do not run the render in this call, and do not set or guess maxCredits yourself — I will set maxCredits to exactly the quoted figure in a separate render request only if the quoted total is $4.32 or less.

**Done**

2026-11-14 02:22 UTC, spent $0.02

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "quote": {
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
    ],
    "expectedSeconds": 15.083,
    "priceUsd": 4.312,
    "maximumUsd": 4.312,
    "priceCredits": 2156,
    "maximumCredits": 2156,
    "currency": "USD",
    "maxCredits": 3200,
    "withinBudget": true
  },
  "balanceCredits": 1023.561
}
```
