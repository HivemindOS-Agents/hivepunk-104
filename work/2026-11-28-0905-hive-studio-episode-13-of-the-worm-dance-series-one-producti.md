# Hive Studio: episode 13 of the worm dance series, ONE production. First re-read the studio guide, then quote it: vertical 9:16, one shot, mode text, model seedance-2.5-higgsfield-account, sound model, 30 seconds. Account line tells the length: if it says ready at 30 seconds, keep 30s; if it caps today's episode at 15 seconds, plan 15s. Prompt (adjust beat timings to the quoted length, keep the look wording identical): a small bright red cartoon worm with big round white googly eyes and black pupils, a shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, clean vector cartoon look, upright and in frame. Shot 1 (0-4s): bouncy chicken-strut dance, flippers out, head bobbing forward and back. Shot 2 (4-9s): tries a spin on one flipper that speeds into a wobble and nearly topples. Shot 3 (9-15s): catches itself, tips its top hat, big proud bow to camera. Stay within the spend limit; report the finished video link and what it cost.

**Failed**

2026-11-28 09:05 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (2 calls): tokens not reported. Known cost $0.0106; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "production": {
    "id": "prod_31a4fdfc1973d72308bb621e996b99e2",
    "status": "queued",
    "title": "Worm dance, episode 13",
    "shotCount": 1,
    "createdAt": "2026-11-28T09:05:45.335Z",
    "updatedAt": "2026-11-28T09:05:45.335Z",
    "finishedAt": null,
    "cancelRequested": false,
    "plan": {
      "title": "Worm dance, episode 13",
      "characters": [],
      "shots": [
        {
          "mode": "text",
          "prompt": "a small bright red cartoon worm with big round white googly eyes and black pupils, a shiny black top hat set straight on its head, two stubby flippers, on a plain seamless turquoise-mint stage, flat even lighting, clean vector cartoon look, upright and in frame. Shot 1 (0-4s): bouncy chicken-strut dance, flippers out, head bobbing forward and back. Shot 2 (4-9s): tries a spin on one flipper that speeds into a wobble and nearly topples. Shot 3 (9-15s): catches itself, tips its top hat, big proud bow to camera.",
          "seconds": 15,
          "model": "seedance-2.5-higgsfield-account"
        }
      ],
      "sound": {
        "mode": "model"
      },
      "captions": [],
      "aspect": "9:16",
      "maxCredits": 2500,
      "keyframeModel": "gpt-image-2-image-to-image"
    },
    "quote": {
      "priceCredits": 50,
      "maximumCredits": 50,
      "priceUsd": 0.1,
      "expectedSeconds": 15,
      "items": [
        {
          "kind": "shot",
          "shotIndex": 0,
          "model": "seedance-2.5-higgsfield-account",
          "priceUsd": 0,
          "maximumUsd": 0,
          "accountCredits": 105
        },
        {
          "kind": "assembly",
          "model": "studio-assembly",
          "priceUsd": 0.1,
          "maximumUsd": 0.1
        }
      ],
      "way": "account",
      "minutes": 10,
      "account": {
        "service": "higgsfield",
        "agent": "Rick",
        "ready": true,
        "seconds": 15,
        "credits": 105,
        "balance": 1638.3,
        "plan": "ultra",
        "today": {
          "clips": 0,
          "most": 3
        },
        "pace": {
          "month": 3000,
          "weekUsed": 0,
          "weekMost": 700,
          "episodeSeconds": 30,
          "nextAt": null
        }
      }
    },
    "shots": [],
    "assemblyFee": "pending",
    "billing": "Each keyframe and shot is held and settled by Managed Media on your credits; a failed generation is refunded there. The assembly fee is charged once, when the finished video is delivered. A cancelled production stops launching new generations; ones already running finish and are charged. A production that rendered every shot but failed before they were cut together keeps its clips: productions.finish makes the cut from them, so nothing is rendered or charged a second time. A shot made on your holder's own Higgsfield account costs no HivemindOS credits: it is paid in that account's own credits, the figure the quote's account line shows, and only cutting it is charged here. Shots made on a rented GPU are not charged by the clip: the machine is rented on your credits for the production, charged by the GPU rentals service for the minutes it ran (it holds ten minutes at a time and gives back what was not used; the quote's rental line is its expected and its most), and given back when its clips are made, when the production fails and when it is cancelled."
  }
}
```
