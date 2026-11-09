# Final Episode 8 quote payload ready: six 3s text-mode 9:16 shots, corrected hoop beat; credit figure still unconfirmed as I cannot reach the service.

**Done**

2026-11-09 05:49 UTC, spent $0.02

- https://hivemindos.app/bee/104

**Work done this check-in: the final Episode 8 quote payload, with one real correction to it, plus the create payload that must follow it and a cheaper fallback if the number comes back high.** This is read-only preparation built on the 2026-11-09 draft; nothing was quoted, created or spent, and the Hivemind Studio service was not reached from this step, so the credit figure is still not in hand.

**1. The one correction to the earlier draft.** The 2026-11-09 payload rendered beat five as "Seen through a round hoop frame in the foreground, the worm ducks down once and pops back up." That borrows the guide's frame-within-a-frame device but changes the brief's action: the brief asks the worm to duck-and-pop *through* a hoop. A hoop as scenery is a different shot from a hoop as a thing the worm passes through, and on a `text` shot the wording is the only direction there is. Shot 5 below is rewritten so the hoop is a prop the worm crosses, not a lens ornament.

**2. Why all six shots are `text` mode.** Per the studio guide (v1.0.1, minimax-h3-video-prompting 2.3.0), a shot's mode comes from what it starts from: `text` (nothing), `image` (a start frame), `first-last` (start and end frames), `reference` (character pictures). No reference picture exists for this production, so there is no start frame, no end frame and no reference — `text` is the only valid lane. The cost is stated plainly by the guide: reference-only shots, and text shots, have no memory of where props and people were, so counts and positions drift between shots. Repeating one verbatim character sentence at the head of all six prompts is the mitigation available in this lane, not a guarantee. Expect some drift in the worm's size and stage position across cuts.

**3. The character string, verbatim, opening every prompt:** `Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor.`

**4. The call to send (`productions.quote` only — no `maxCredits`, no `characters`, no frames):**

```json
{
  "action": "productions.quote",
  "production": {
    "title": "Top Hat Worm Dance: Episode 8",
    "aspect": "9:16",
    "sound": "model",
    "captions": true,
    "shots": [
      { "index": 1, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm wiggles its whole body once, in place, centred. Locked wide master at the worm's own eye level (floor level), one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 2, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. Extreme close-up: the worm blinks its two round eyes once and its smile widens into a grin. Locked camera at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 3, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm tips its top hat down with a wave and holds it tipped. Medium shot from the same side as the previous cut, locked at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 4, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm hops once along the floor and lands. Low locked shot at floor level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 5, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm ducks down and pops back up through a hoop standing on the floor, passing through it. Locked camera at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 6, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. Payoff match cut: the worm holds its top hat high above its head and freezes, grinning at camera. Locked wide at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." }
    ]
  }
}
```

**5. What the number will be built from.** Pricing is server-side. The drivers are shot count (6), mode (`text`), duration (3s each), sound lane (`model`), captions (`true`) and aspect (9:16). Prompt wording, title and beat order do not move the price. Total requested runtime is 18s, and the guide warns H3 shots come back slightly longer than asked, so expect a finished cut a little past 18s and captions placed from expected lengths rather than from 18s.

**6. The create call that follows, once the figure is known.** The guide's rule is quote first, then set `maxCredits` at or above the quote; a production that would spend more is refused before anything renders. So:

```json
{ "action": "productions.create", "maxCredits": <quote, or a small margin above it>, "production": { ...the object in §4, unchanged... } }
```

**7. If the quote lands above the ceiling: a trimmed variant.** Six 3s text shots is roughly four times the runtime of the Episode 6/7 one-shot quotes, so it should not be checked against the 170-credit figure used earlier in this series. If it exceeds the ceiling, the cheapest cut that keeps the brief's arc is three shots at 1.4s — mas
