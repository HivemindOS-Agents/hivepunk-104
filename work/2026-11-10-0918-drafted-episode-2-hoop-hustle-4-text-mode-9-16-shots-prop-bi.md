# Drafted Episode 2 'Hoop Hustle': 4 text-mode 9:16 shots, prop bible, create/poll payloads and a 1500-credit fallback ladder; quote and video link unconfirmed (Studio unreachable here).

**Done**

2026-11-10 09:18 UTC, spent $0.05

- https://hivemindos.app/bee/104

**Episode 2 — "Hoop Hustle" (4 shots, 9:16, text mode only)**

**Decision taken this step:** per your instruction I skipped re-returning the guide and went straight to the production plan for this new shot list. All four shots are **text mode** as the brief demands, with no reference image and no invented picture links. Note the known trade-off: the guide says text/reference lanes have no memory of prop position, so the worm and hoop can drift between cuts. I mitigate it the only way text mode allows — one verbatim character+prop block repeated in every shot prompt, and one locked floor-level master framing that shots 1 and 4 both return to.

**I could not call `productions.quote` from this step, so the exact credit number is unconfirmed.** Everything else is production-ready.

---

### Call 1 — quote

`productions.quote` with the plan below, `aspect: "9:16"`, `sound: "model"`, 4 shots × 2.5s requested, no reference images, no start/end frames.

Expected: H3 returns shots slightly longer than asked, so 2.5s requested ≈ **2.8s effective each ≈ 11.2s cut** ("about 10s"). Captions, if any, must be timed from the 2.8s figures, not the 2.5s request.

### Prop bible (checked against every shot)

| Prop | Count | State |
|---|---|---|
| Chubby red worm (2 googly eyes, wide grin) | 1 | in every shot |
| Small black top hat | 1 | on the worm's head, shots 1–3; hoop lands on it in shot 4 |
| Yellow hula hoop | **1 only** | around worm's middle (1–2), airborne screen-right (3), resting on hat brim (4) |
| Small wooden crate stage | 1 | under the worm, shots 1, 3, 4 |
| Red velvet curtains, left + right | 2 panels | same position every shot |

Screen direction held: the hoop leaves frame **screen-right** in shot 3 and re-enters from above in shot 4 — no reversed frames anywhere.

### Character block — copy verbatim into all four prompts

> One character only: a chubby red cartoon worm with two big googly eyes, a wide cheerful grin, and a small black top hat worn straight on its head. Same worm, same proportions, same hat in every shot.

### Shot list

1. **Wide master, ~2.5s** — "Locked wide shot, camera at floor level, crisp neutral stage lighting, short shadows, no orange or golden tint anywhere. [character block] The worm balances on top of a small wooden crate that serves as a tiny stage, flanked by two red velvet curtains hanging left and right. One yellow hula hoop spins around the worm's middle while its body sways in time. One hoop only, staying around the worm's body for the whole shot."
2. **Extreme close-up, ~2.5s** — "Extreme close-up on the worm's face, same crate stage, the two red velvet curtains soft and blurred behind. [character block] Its two googly eyes cross inward and wobble as it strains to keep the rhythm; the spinning yellow hoop is a blurred band across the foreground. One hoop only."
3. **Medium, ~2.5s** — "Medium shot from the same side, same crate stage and red curtains. [character block] The worm swivels its hips wildly, body whipping side to side, and the yellow hoop slips upward off its body, flying up and toward screen-right, leaving the frame. One hoop only."
4. **Wide payoff, ~2.5s** — "Locked wide shot back at floor level, same crate stage and red curtains. [character block] The yellow hoop drops straight down and settles around the worm's black top hat, resting on the brim. The worm holds a proud bow, head tipped forward. One hoop only, now resting on the hat."

Each cut shows something new: master → face → action → payoff.

### Call 2 — create

```json
{
  "title": "Daily Worm Ep.2 - Hoop Hustle",
  "aspect": "9:16",
  "maxCredits": 1500,
  "sound": "model",
  "shots": [
    { "mode": "text", "duration": 2.5, "characters": [], "prompt": "<shot 1 text>" },
    { "mode": "text", "duration": 2.5, "characters": [], "prompt": "<shot 2 text>" },
    { "mode": "text", "duration": 2.5, "characters": [], "prompt": "<shot 3 text>" },
    { "mode": "text", "duration": 2.5, "characters": [], "prompt": "<shot 4 text>" }
  ]
}
```

`mode`, `duration`, `aspect`, `sound`, `characters`, `prompt` are the field names the guide uses. `title` is inferred — check it against the live schema at call time and drop it if rejected. No `startImageUrl`, no `endImageUrl`, no `referenceImageUrl` on any shot: text mode takes nothing, and the brief forbids reference images. `maxCredits` is set at 1500, at or above the quote, so the run is not refused before rendering.

### Call 3 — poll to finished

Poll the production every 20–30s until status is finished, cap ~15 minutes. If it errors, retry the identical plan once. Return the finished video's link, not an intermediate job URL.

### Reply to you (filled at run time)

> Episode 2 "Hoop Hustle" — 4 shots, 9:16, all text mode, no reference image.
> Quote: **<N> credits** (maxCredits 1500).
> Credits spent: **<N>**.
> Video: **<link>**

### If the quote lands above 1500 (fallback ladder, in order)

1. `sound: "silent"` — drops the per-second scoring cost, keeps all four shots.
2. Durations 2.5s → 2.0s each (≈9s cut).
3. Drop shot 2 and rebalance to three shots at 3.2s, keeping the master/action/payoff beats.

Never exceed 1500: a production over the cap is refused before anything renders.

**Left for you (owner):** the quote, create and poll calls run in Hivemind Studio, which I can't reach from this step — paste the four prompts in, then send me back the quote and the finished link.
