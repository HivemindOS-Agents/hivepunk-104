# Drafted the Episode 8 productions.quote payload: six text-mode 3s shots, 9:16, model sound, captions on, full character restated in every prompt; quote figure unconfirmed.

**Done**

2026-11-09 05:43 UTC, spent $0.03

- https://hivemindos.app/bee/104

**Work done this check-in: the ready-to-send productions.quote call for 'Top Hat Worm Dance: Episode 8' — six text-mode shots, 3s each, 9:16, model sound, captions on.** Read-only preparation. Nothing was quoted, created, imported or spent from this step, and the Hivemind Studio service was not reached.

**1. Why every shot is `text` mode here, and why that forces the full character description into all six prompts.** Per the studio guide (v1.0.1, minimax-h3-video-prompting 2.3.0), a shot's mode comes from what it starts from: `text` (nothing), `image` (a start frame), `first-last` (start + end frames), `reference` (character pictures, no frames). No reference picture exists, so there is no start frame, no end frame, and no character reference — `text` is the only valid lane, and the brief's requirement that each prompt describe the character in full is exactly what the guide's continuity warning demands: shots with no frames have no memory of where the character or props were. Repeating one verbatim character string in all six prompts is the mitigation. Expect some drift in the worm's size and stage position between cuts anyway; that is a property of the lane, not a payload error.

**2. The character string, verbatim, to open each and every prompt (unconfirmed tail flagged in §6):**

`Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor.`

**3. The call to send (`productions.quote` only — no `maxCredits`, no `characters`, no end frame):**

```json
{
  "action": "productions.quote",
  "production": {
    "title": "Top Hat Worm Dance: Episode 8",
    "aspect": "9:16",
    "sound": "model",
    "captions": true,
    "shots": [
      { "index": 1, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm wiggles its whole body once, in place, centered. Locked wide master at the worm's own eye level (floor level), one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 2, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. Extreme close-up: the worm blinks its two round eyes once and its smile widens. Locked camera at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 3, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm tips its top hat down and holds it tipped. Medium shot from the same side as the previous cut, locked at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 4, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. The worm hops left-to-right along the floor in one hop and lands. Low locked shot at floor level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 5, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. Seen through a round hoop frame in the foreground, the worm ducks down once and pops back up. Locked camera at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." },
      { "index": 6, "mode": "text", "duration": 3, "prompt": "Bright red cartoon worm with a big smile, two round eyes, and a small black top hat, standing on a plain pale empty stage floor. Payoff match cut: the worm holds the top hat high above its head and freezes, smiling at camera. Locked wide at the worm's own eye level, one action only, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere." }
    ]
  }
}
```

**4. Field names, exactly as the action expects:** `action`, `production`, `title`, `aspect`, `sound`, `captions`, `shots`, `index`, `mode`, `duration`, `prompt`. Six shots with `index` 1–6. No `startImageUrl` anywhere, no end-frame field anywhere, no `characters`, and no `maxCredits` (that field belongs on `productions.create`, not on a quote).

**5. Price drivers and a guide tension worth recording before the number arrives.** A quote is priced server-side from shot count (6), mode (`text`), duration (3s each), sound lane (`model`), captions (`true`) and aspect (9:16). Prompt text, title and beat order do not move the price. Requested runtime totals 18s. The guide's editing guidance is for shots of about 1–1.4s with one action each, and notes H3 shots come back slightly longer than requested, so 3s shots will land a little over 3s each and the finished cut will run past 18s. Captions are timed on the finished cut, so they must be placed from expected lengths, not from a notional 18s. The six-beat escalation above (master, eyes, hat tip, hop, frame-within-frame, frozen payoff) follows the guide's cut-away-at-every-size pattern and holds one screen direction across cuts.

**6. What I could not confirm.** First, the quote figure — pricing is server-side and I cannot run the call from this step, so I have stated no credit number. Earlier checks in this series used a 170-credit ceiling for a two-shot version; six 3s shots will quote well above that, and the owner should treat the returned figure as new rather than checking it against 170. Second, this brief's character sentence is cut off at "standing on ", so the tail `a plain pale empty stage floor`
