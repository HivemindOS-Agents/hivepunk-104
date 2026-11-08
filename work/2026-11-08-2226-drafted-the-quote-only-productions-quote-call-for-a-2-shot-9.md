# Drafted the quote-only productions.quote call for a 2-shot 9:16 'Top Hat Worm Dance: Episode 6' (maxCredits 170, sound model), with guide rules, prop bible; price formula unconfirmed.

**Done**

2026-11-08 22:26 UTC, spent $0.02

- https://hivemindos.app/bee/104

DRAFT — productions.quote call for 'Top Hat Worm Dance: Episode 6', 2 shots, no create, no spend

Scope check: this step is quote-only. No production is created, no credits are spent, and nothing is purchased. The quote is a read of the pricing engine; the single owner-side action it needs is the call itself, run from an account that holds the studio session.

Guide read first. The accepted schema I am drafting against is from the studio guide, source `minimax-h3-video-prompting 2.3.0` (version 1.0.1), sections `spec` and `planning`. The rules that bind this call:
- Quote first and set `maxCredits` at or above the returned quote, or the production is refused before anything renders. A quote is not a charge.
- Pick each shot's mode from what it starts from: `text` (nothing), `image` (a start frame), `first-last` (start and end frame), `reference` (character pictures, no frames).
- Frame modes for any multi-shot story; reference-only shots lose prop and person positions between shots.
- Never give a reference shot a start or end frame — the reference lane drops frames silently.
- `keyframeEdit` edits `startImageUrl` when one is given, else draws from the shot's character references. `endFrameEdit` always edits that shot's own start frame, so a start/end pair shares one camera.
- List in `characters` only who appears in the shot.
- Captions are timed on the finished cut, so H3 shots run slightly longer than the requested duration.
- `sound: "model"` keeps the models' own audio; `"remaster"` is scored and priced by the second; `"silent"` lays a silent track. `model` is the lane with no second-based sound charge.
- Keep the aspect at 9:16 and draw every keyframe at 9:16.
- Planning rules for a 2-shot cut: home-base master locked wide at the subjects' own eye level (floor level for floor play), every later shot opening on an edit of that wide; one action per shot; hold one screen direction; write the daylight phrase verbatim.

--- CALL: productions.quote (the only call in this step) ---
{
  "title": "Top Hat Worm Dance: Episode 6",
  "aspect": "9:16",
  "sound": "model",
  "captions": true,
  "maxCredits": 170,
  "characters": [
    {
      "id": "worm",
      "name": "Top Hat Worm",
      "description": "a stout cartoon red worm wearing a black top hat; identical appearance in every shot"
    }
  ],
  "shots": [
    {
      "id": 1,
      "mode": "text",
      "duration": 1.2,
      "characters": ["worm"],
      "prompt": "Locked wide master at floor level, camera at the worm's own eye level, no camera movement. Plain empty room: bare neutral walls, plain floor, nothing else in frame. Crisp neutral daylight, short shadows, no orange or golden tint anywhere. A stout cartoon red worm wearing a black top hat, centered, body pointing camera-right. One action: the worm wiggles its whole body."
    },
    {
      "id": 2,
      "mode": "image",
      "duration": 1.2,
      "characters": ["worm"],
      "startImageUrl": "<keyframeEdit of shot 1's start frame: same wide, same light, worm moved a step toward camera>",
      "prompt": "Match-cut punchline, medium shot in the same plain empty room, same black top hat, crisp neutral daylight, short shadows, no orange or golden tint anywhere. Same screen direction - the worm still faces camera-right. One action: the worm tips the brim of its top hat and wiggles the hat as if the hat is dancing too."
    }
  ]
}

--- HOW THE 2-SHOT VERSION DIFFERS FROM THE EARLIER 3-SHOT DRAFT ---
The earlier package on this title used three shots at a provisional `maxCredits` of 60. This step fixes the ceiling at the owner's stated 170 and drops to two shots, so the reaction close-up from the 3-shot plan is cut and its beat folded into shot 2's prompt. Shot 2 uses `keyframeEdit` on shot 1's start frame, not `endFrameEdit`, because with only two shots there is no third shot to hand a camera to; keeping the edit anchored to shot 1's wide is what holds camera geometry and the hat's position across both cuts. Both shots are frame-consistent, no `reference` mode anywhere, so the silent-frame-drop trap does not apply.

PROP BIBLE (checked against every keyframe and clip before any create)
- Worm: one, stout, bright red, no limbs, in both shots, same silhouette across the cut.
- Top hat: one, black, on the worm's head, brim parallel to the floor. Shot 1 resting; shot 2 tipped and wiggled by the worm. One hat only - no second hat, no colour shift.
- Room: zero props. Plain walls, plain floor, empty in both shots.
- Light: one neutral daylight source, key from camera-left, short floor shadows, no orange or golden tint. The phrase is written verbatim in both prompts.
- Screen direction: worm faces camera-right in both shots. A reversed frame cannot be fixed in the edit and would have to be redrawn.

DURATION AND CAPTION NOTE
Requested total 2 x 1.2s = 2.4s; expect roughly 2.6-3.4s finished, since H3 shots come back slightly longer than asked. Captions are timed on the finished cut, so time them against the finished lengths, not 1.2s.

COST: NOT CONFIRMED, AND NOT GUESSED
I will not invent a figure. The copy of the guide I hold truncates inside the `planning` section, before the per-shot and per-remaster-second price table, so the formula is not on disk here. What the guide does establish: `sound: "model"` is not charged by the second the way `remaster` is, so this is the cheaper of the two scored lanes for a short cut; and 170 is a ceiling, not a price - if the returned quote exceeds 170, set `maxCredits` at or above it or leave it, but the call itself spends nothing either way. Pass or fail the budget test only after the quote number exists.

WHAT I COULD NOT CONFIRM
1. The price formula, and therefore whether this 2-shot cut lands under 170. No number is asserted above.
2. The exact field names for character reference pictures; the guide text here truncates before that part of the schema, so the shape above mirrors previously accepted quote calls on this same title.
3. The charac
