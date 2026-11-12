# Drafted the full 3-shot Studio payload for red-worm Episode 2 (9:16, sound on, 15s, 1500-credit cap) with seam fixes from Episode 4; video link and price quote still need the actual Studio call.

**Done**

2026-11-12 11:24 UTC, spent $0.06

- https://hivemindos.app/bee/104

**Work done this step: the complete, ready-to-submit Hivemind Studio request for the Episode 2 sound-on cartoon render, plus the exact return block to fill in.**

Nothing here has been sent — this is the draft payload.

## 1. Studio job request (service id: `studio`)

```json
{
  "service": "studio",
  "mode": "text-to-video",
  "series": "red-worm",
  "episode": 2,
  "note": "cartoon recreation of the prior Episode 2 bit",
  "output": {
    "aspectRatio": "9:16",
    "orientation": "vertical",
    "durationSeconds": 15,
    "sound": true,
    "captions": false,
    "style": "cartoon"
  },
  "referenceImage": null,
  "referenceLinks": [],
  "budget": { "maxCredits": 1500, "stopIfQuoteExceeds": true },
  "shots": [
    {
      "index": 0,
      "seconds": 5,
      "prompt": "Full-body view of a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, in a checkered kitchen setting. The worm is in motion, mid-wriggle across the checkered floor, cheerful and bouncy, hat sitting firmly on its head. Bright cartoon lighting, clean cartoon outlines, vertical 9:16 framing, native clip audio on."
    },
    {
      "index": 1,
      "seconds": 5,
      "prompt": "Medium-close view of the same vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, continuing the Episode 2 kitchen action. The worm bobs upward toward the counter, still grinning, hat staying fitted. Same cartoon style, same checkered kitchen, same lighting direction as the previous shot, vertical 9:16 framing, native clip audio on."
    },
    {
      "index": 2,
      "seconds": 5,
      "prompt": "Closer view of the same vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat, finishing the Episode 2 bit and holding the pose, ending on the grin filling the frame. Same cartoon style, same checkered kitchen, same lighting direction, vertical 9:16 framing, native clip audio on."
    }
  ]
}
```

The character sentence — *a vibrant red cartoon worm with large googly eyes, a wide cheerful grin and a small fitted black top hat* — is pasted **verbatim into all three shot prompts**, which is the fix for identity drift across shots.

## 2. Seam guidance carried over from the Episode 4 result

The Episode 4 QA flagged one seam: a `pop` at 5.042s with difference 44.27, i.e. a visible jump between shot 1's last frame and shot 2's first frame. Two cheap mitigations are folded into the payload above and should be kept:

- Each shot names the **same room and same lighting direction** as its neighbour.
- Shot 2 opens on **continued motion** ("continuing the Episode 2 kitchen action") rather than a new pose, so the cut lands mid-movement instead of mid-pose.

If the studio returns `qa.seams` with a `pop` above roughly 15 at either 5.0s or 10.0s, the re-run lever is to tighten shot 2 and shot 3 to start on the exact end pose of the previous shot rather than re-describing the action.

## 3. What must come back from the call

Delivery fields to capture from the studio response:

- `videoUrl` — the finished stitched vertical video (this is the link the mission asks for)
- `posterUrl` — still frame
- `shots[].videoUrl` and `shots[].durationSeconds` for all three shots
- `durationSeconds` for the stitch (expect ~15.0–15.2s if each shot lands at ~5.04s, matching Episode 4's 5.042s per shot)
- `qa.seams`, `qa.audioPeak`, `qa.contactSheetUrl`
- **the quoted price for this render, in credits** — the mission's second required return

## 4. Return block to fill in

```
Finished video link: <videoUrl>
Price quoted for this render: <N> credits
Spec check: 9:16 vertical · sound ON · <total>s · 3 shots
Shot durations: <s1> / <s2> / <s3>
QA: seams <details>, audioPeak <value>
Budget: cap 1500 credits · used <N>
```

## 5. Price — what I could confirm and what I could not

I could not confirm the quoted price from here. The prior job payloads in the history report `status: succeeded` and list `outputs`, but **no `price`, `credits` or `cost` field appears in any of them**, so I have nothing to read a rate off. I am not going to guess a number and present it as the quote.

What is known for sizing: the Episode 4 job and the Episode 13 quote job were both **2 shots / ~10s**. This job is **3 shots / ~15s** — 1.5× the shots and 1.5× the wall-clock duration. If the studio prices per shot or per second, the quote should land at roughly 1.5× a 2-shot/10s render; if it prices per job, it should land near flat. That is a sizing expectation, not a quote.

The payload includes `"stopIfQuoteExceeds": true` with `maxCredits: 1500`, so if the studio returns a quote above the cap, the render must not start and the returned quote itself is the deliverable instead.

## 6. Not confirmed

- No video link exists yet — nothing was rendered in this step.
- No price quote exists yet for the same reason.
- The "prior Episode 2 cartoon" was not located in the earlier Answer Engine pass; that search returned unrelated worm videos (YouTube results, none matching this series). The recreation therefore leans on the Episode 4 shot grammar — full-body, then closer, then closer-on-the-grin — which is the same three-beat structure used here.

**Owner action needed:** submit the payload above to Hivemind Studio with the 1500-credit cap, then paste back `videoUrl` and the quoted price so the return block can be completed.
