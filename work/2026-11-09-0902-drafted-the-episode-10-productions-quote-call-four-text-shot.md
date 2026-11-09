# Drafted the Episode 10 productions.quote call: four text shots at 6.25s, 9:16, model sound, captions on; flagged truncated opener and 6.25s vs guide rhythm. Quote figure unconfirmed.

**Done**

2026-11-09 09:02 UTC, spent $0.04

- https://hivemindos.app/bee/104

**Episode 10, this check-in: the `productions.quote` call in final draft form — four `text` shots at 6.25s, 9:16, sound `model`, captions true — plus the caption script re-timed for 6.25s windows and two carry-over flags.** Read-only preparation. This step is quote only: no create, no import, no render, no spend. I did not reach the Hivemind Studio service, so the credit figure is still not in hand. The Episode 8 payloads (work/2026-11-09-0606 and -0618) are superseded by this object and are not restated.

**1. The call to send (`productions.quote` only — no `maxCredits`, no `characters`, no start frame, no end frame):**

```json
{
  "action": "productions.quote",
  "production": {
    "title": "Top Hat Worm Dance: Episode 10",
    "aspect": "9:16",
    "sound": "model",
    "captions": true,
    "shots": [
      { "index": 1, "mode": "text", "duration": 6.25, "prompt": "Bright red cartoon worm with a cheerful grin, two big round eyes and a small black top hat, standing on a plain pale empty stage floor. The worm wiggles its whole body once, in place, centred, locked off with no camera move. One action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 2, "mode": "text", "duration": 6.25, "prompt": "Bright red cartoon worm with a cheerful grin, two big round eyes and a small black top hat, standing on a plain pale empty stage floor. The worm tips its top hat down with a wave and holds it tipped, then settles. One action only, medium shot from the same side as the previous cut, locked at the worm's own eye level, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 3, "mode": "text", "duration": 6.25, "prompt": "Bright red cartoon worm with a cheerful grin, two big round eyes and a small black top hat, standing on a plain pale empty stage floor. The worm hops once along the floor and lands, then stays put. One action only, low locked shot at floor level, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 4, "mode": "text", "duration": 6.25, "prompt": "Bright red cartoon worm with a cheerful grin, two big round eyes and a small black top hat, standing on a plain pale empty stage floor. Payoff match cut: the worm holds its top hat high above its head and freezes, grinning at camera. One action only, locked wide at the worm's own eye level, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." }
    ]
  }
}
```

Field names as the action expects: `action`, `production`, `title`, `aspect`, `sound`, `captions`, `shots`, `index`, `mode`, `duration`, `prompt`. Four shots, `index` 1–4, duration 6.25 on all four. No `startImageUrl`, no end-frame field, no `characters`, no `maxCredits` — the last belongs on `productions.create`, never on a quote. Every shot is `text` mode because there is no reference picture: `text` is the only lane that needs no start frame, no end frame and no character reference. That also means the worm's size and stage position will drift between cuts; repeating the verbatim opener is the mitigation available, not a guarantee.

**2. Flag — the opener sentence is cut off in the brief.** It reads "Bright red cartoon worm with a cheerful grin, two big rou" and stops mid-word. I completed it as `two big round eyes and a small black top hat, standing on a plain pale empty stage floor.`, which matches the character sentence used across the Episode 8 payloads. That clause is the only thing to change in all four prompts if the owner's intended tail differs.

**3. Flag — 6.25s is far above the studio guide's cut rhythm.** The guide's editing guidance is roughly 1–1.4s per shot with one action each. Four shots at 6.25s request 25s of generation, and the guide warns shots come back slightly longer than asked, so expect a finished cut near 26–27s, not 25s. A single action filling 6.25s will read as slow; the camera-lock and "then settles / then stays put" clauses in shots 2 and 3 are there to give the action a resting tail rather than a repeat. If the quote comes back above the ceiling, the cheapest lever is duration, not shot count: 4 × 1.5s keeps all four beats at 6s requested, the same shape as the Episode 8 tier-B fallback. Quote each shape separately — one quote cannot price another.

**4. Caption script for 6.25s windows.** The one-beat words written for Episode 8's 1.5s windows are no longer forced by width; at 6.25s a full phrase fits easily. The risk inverts: a caption can outlast its action. Hold one caption per shot rather than splitting into two.

| # | beat | caption to see | cue to hear |
|---|---|---|---|
| 1 | body wiggle | wiggle wiggle | soft bounce, no voice |
| 2 | hat tip | tip of the hat | single chime |
| 3 | floor hop | boing! | boing |
| 4 | hat held high, frozen | ta-da! | ta-da sting |

With sound `model` and captions on, the service times captions against the finished cut, so this is a script to aim for, not a timing I can set. If a caption crosses a cut, the fix is a caption edit on the cut, not a re-render.

**5. Carry-over flag, unresolved.** The most recent Episode 8 run in this series returned one media URL ending `.jpeg` — a still image, not a video. Either the service returned a poster frame while the video renders separately, or the request produced an image instead of a video. I cannot tell which from here, and the brief's "finished video link" was never in hand. Worth settling before the Episode 10 create call, because the same shape may recur.

**6. What I could not confirm.** The quote figure — pricing is server-side and this step cannot run the call, so no credit number is stated and I cannot say whether it lands at or under the 1500 ceiling. Whether the four dance actions in §1 are the owner's intended four; the brief supplied the opener only, so the beat list is my draft built from the Episode 8 arc (wiggle, hat tip, hop
