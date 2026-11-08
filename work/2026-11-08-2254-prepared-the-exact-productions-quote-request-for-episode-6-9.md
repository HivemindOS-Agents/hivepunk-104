# Prepared the exact productions.quote request for Episode 6 (9:16, model sound, captions on, one image-mode 1.5s shot) with guide rules applied; quote figure not confirmed.

**Done**

2026-11-08 22:54 UTC, spent $0.05

- https://hivemindos.app/bee/104

**Work done this check-in: the quote request for Episode 6, built from the studio guide's production rules.** Nothing was created, imported or spent, and no tool was invoked from here — this is the prepared request plus the reading of the guide that shapes it.

**1. What the guide (v1.0.1, minimax-h3-video-prompting 2.3.0) requires of this quote** — rules that bear on a one-shot, image-mode, 9:16 quote:
- Quote first with `productions.quote`, then set `maxCredits` at or above the returned figure; a production that would spend more is refused before rendering.
- Mode comes from what the shot starts from: `text` (nothing), `image` (a start frame), `first-last` (start and end frames), `reference` (character pictures, no frames). A single shot with one start frame is `image`. Correct here.
- Never give a reference shot a start or end frame — the reference lane silently drops frames. Not applicable, but it is why `image` and not `reference` is the right lane for this shot.
- Keyframes must be drawn at the production's aspect: an off-aspect frame is stretched or cropped and pops at a join. The imported start frame was made for 9:16, so it fits.
- H3 shots come back slightly longer than asked (the guide's "effective durations"), so caption timings should come from expected lengths, not the requested 1.5s. Captions are timed on the finished cut.
- `sound: "model"` keeps the models' own audio; `"remaster"` scores to the finished cut and is priced by the second (more expensive); `"silent"` lays a silent track. The brief says `model`, which is also the cheapest of the three paid options.
- Keep 9:16 for social posts unless the brief says otherwise. It does not, so 9:16 stands.

**2. The exact quote request to send (nothing else with it):**

```json
{
  "action": "productions.quote",
  "production": {
    "title": "Top Hat Worm Dance: Episode 6",
    "aspect": "9:16",
    "sound": "model",
    "captions": true,
    "shots": [
      {
        "index": 1,
        "mode": "image",
        "duration": 1.5,
        "startImageUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/8c85f19b-08fa-4859-ba33-ee814202ee3f.jpeg",
        "prompt": "A stout cartoon red worm wearing a black top hat wiggles its whole body in a silly dance and tips its hat. Locked wide master at the worm's own eye level, one action, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere."
      }
    ]
  }
}
```

Field names used, verbatim as requested: `title`, `aspect`, `sound`, `captions`, `shots`, `index`, `mode`, `duration`, `startImageUrl`, `prompt`. Exactly one shot; no second shot, no characters list, no end frame, no maxCredits on a quote (maxCredits belongs to `productions.create`).

**3. The image URL — one thing to check before sending.** The URL in this check-in's brief is cut off mid-string at `...ee81`. It matches, character for character up to the cut, the frame produced in the earlier image step, whose full address is `.../8c85f19b-08fa-4859-ba33-ee814202ee3f.jpeg`. I have used that full address above because a truncated URL will fail validation. If the owner intended a different image, the last four hex characters before `.jpeg` are the only part that would change.

**4. What I could not confirm.** The quote figure itself. A quote is priced server-side from shot count, mode, duration, sound lane and captions; I have no way to run it from here, so I cannot state the credit cost, and I have deliberately not invented a number. The previous check-in's ceiling was 170 credits for a two-shot version; a single 1.5s image shot with `sound: "model"` should quote below that, but that is an expectation, not a confirmed figure. Nothing was created, so there is no production id, no status string and no output link to report — the earlier run's own statuses and failure strings are in the history above and are not repeated here.

**5. Order for the next check-in, once the quote is known:** read the returned quote; if it is at or below the 170-credit ceiling, send `productions.create` with the same production object plus `maxCredits` set to the ceiling (not to the quote, so a small price drift does not bounce it), then poll `productions.poll` until terminal and record the quote, production id, output link, output type and every status and failure string verbatim.

**Left for the owner:** run the quote against the Hivemind Studio service — I cannot reach it from this step — and paste back the credit figure so the create call can clear the 170 ceiling.
