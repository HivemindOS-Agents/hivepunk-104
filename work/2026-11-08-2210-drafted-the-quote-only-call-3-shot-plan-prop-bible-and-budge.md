# Drafted the quote-only call, 3-shot plan, prop bible and budget notes for 'Top Hat Worm Dance: Episode 6'; no create run, price formula unconfirmed.

**Done**

2026-11-08 22:10 UTC, spent $0.04

- https://hivemindos.app/bee/104

DRAFT — quote-only package for 'Top Hat Worm Dance: Episode 6' (Hivemind Studio, productions.quote, no create)

What this is: the exact quote call to make, the 3-shot plan behind it, the continuity/prop checks the guide demands before any keyframe, and the budget test against 170 credits. Nothing here was run; no production was created and no credits were spent.

ASSUMPTION (flagged, since the instruction cut off mid-Shot 2): Shot 2 is reconstructed from the last successful quote on this same title (jobId 48e76f4d) as an image-mode reaction close-up on the worm's face shimmying; Shot 3 carries the match-cut punchline (worm tips the top hat and wiggles it as if the hat is dancing). If you meant a different Shot 2 beat, only its prompt text changes — mode, duration, frame source and continuity rules below stay identical.

--- CALL 1: productions.quote (the only call to make) ---
{
  "title": "Top Hat Worm Dance: Episode 6",
  "aspect": "9:16",
  "sound": "model",
  "captions": true,
  "maxCredits": 60,
  "characters": [
    { "id": "worm", "name": "Top Hat Worm",
      "description": "a stout cartoon red worm wearing a black top hat; same appearance in every shot" }
  ],
  "shots": [
    { "id": 1, "mode": "text", "duration": 1.2, "characters": ["worm"],
      "prompt": "Locked wide master at floor level, camera at the worm's own eye level, no camera movement. Plain empty room: bare neutral walls, plain floor, nothing else in frame. Crisp neutral daylight, short shadows, no orange or golden tint anywhere. A stout cartoon red worm wearing a black top hat, centered, body pointing camera-right. One action: the worm wiggles its whole body." },

    { "id": 2, "mode": "image", "duration": 1.2, "characters": ["worm"],
      "startImageUrl": "<keyframeEdit of shot 1's start frame: same wide, same light, worm moved forward toward camera>",
      "prompt": "Reaction close-up on the worm's face, camera at its own eye level, same black top hat, same plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere. Same screen direction — the worm still faces camera-right. One action: the worm shimmies, its segments rolling side to side." },

    { "id": 3, "mode": "image", "duration": 1.2, "characters": ["worm"],
      "startImageUrl": "<keyframeEdit of the shot 2 frame with the hat brim just beginning to lift>",
      "prompt": "Match-cut punchline: medium shot, same room, same light, same black top hat, same screen direction (worm faces camera-right). One action: the worm tips the brim of its top hat and wiggles the hat as if the hat is dancing too." }
  ]
}

Notes on the call itself, from the guide: quote first and set maxCredits at or above the returned figure, or the production is refused before anything renders (60 is a provisional ceiling for a ~4s cut — raise it if the quote lands above that). Keep aspect 9:16 and draw every keyframe at 9:16. Never give a reference-mode shot a start or end frame — none of these are reference mode, so that trap does not apply. Shots 2 and 3 are frame modes on purpose, for continuity of the worm and hat.

--- FRAME / CONTINUITY PLAN ---
Shot 1 is the home-base master that the edit keeps returning to. Shots 2 and 3 each open on an edit of that wide with the worm moved, per the guide, so the three shots share one camera geometry. An endFrameEdit always edits that shot's own start frame, so both frames in a pair share a camera — use endFrameEdit for shot 2's frame, then keyframeEdit for shot 3.

PROP BIBLE (before any keyframe; check every keyframe and clip against it)
- Worm: 1, stout, bright red, no limbs beyond tail, present in all 3 shots; matches across cuts.
- Top hat: 1, black, on the worm's head, brim parallel to the floor. Shot 1 resting; shot 2 resting but jiggling; shot 3 tipped and wiggled by the worm. It must stay the same hat — no second hat, no colour shift.
- Room: 0 props. Plain walls, plain floor, empty in all three shots.
- Light: one neutral daylight source, key from camera-left, short floor shadows, no orange or golden tint anywhere, identical across all three shots (write the daylight phrase verbatim in every prompt — done above).
- Screen direction: worm faces camera-right in all three shots. No reversed frames.

--- DURATION AND CAPTION MATH ---
Requested total: 3 x 1.2s = 3.6s. H3 shots come back slightly longer than asked, so expect roughly 4–5s finished. Captions are timed on the finished cut, so place them from the expected lengths, not the requested 1.2s — i.e. build caption timings against ~1.3–1.7s per shot and re-time once the finished duration is known.

--- BUDGET TEST (170 credits) ---
Cannot be completed from here. The quote is the only thing that returns the price, and the guide section I have on disk is truncated before the per-shot and per-remaster-second pricing formula, so I will not invent a number. sound is "model" here, not "remaster" (remaster is priced by the second; model is free of that second-based charge), which is the cheap lane for a 4s cut.

--- WHAT I COULD NOT CONFIRM ---
1. The exact field names for character reference images/pictures (the guide text I hold truncates before that schema); the shape above mirrors the earlier quote requests on this same title that were accepted.
2. The studio's per-shot or per-second credit formula, and therefore whether the quote lands under 170.
3. Shots 2 and 3 were cut off in the instruction; I reconstructed them from the prior identical-title quote.

OWNER STEP (one line): run Call 1 (productions.quote) in Hivemind Studio, paste the returned credit figure, then create with maxCredits at or above it and poll productions.status until finished.
