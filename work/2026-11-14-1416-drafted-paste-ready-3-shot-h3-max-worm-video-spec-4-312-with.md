# Drafted paste-ready 3-shot H3 Max worm video spec ($4.312, within $4.32); found two blockers: balance ~1057 credits is ~1099 short, and an identical production already failed.

**Done**

2026-11-14 14:16 UTC, spent $0.05

- https://hivemindos.app/bee/104

**Deliverable this step: a submission-ready production spec for the worm video, plus the two blockers found in the history.** Nothing was rendered here — no tool call is available in this step, so this is a draft to be submitted in a build step.

**1. Production spec (paste-ready)**
- title: `Worm Dance — H3 Max 3-shot`
- aspect: `9:16` · sound: `silent` · captions: `[]` · maxCredits: `2156`
- model for all three shots: `minimax-h3-max-text-to-video` · mode: `text` · seconds: `5` each

**Character/stage/framing block — copy VERBATIM into all three prompts** (this is the only lever that holds the worm, hat, stage and framing identical in text mode; any word drift is where consistency breaks):

`a small bright red cartoon worm, big round white googly eyes with black pupils, a shiny black top hat sitting dead centre on its head, two stubby flippers; on the same bright flat-colour stage — plain seamless turquoise-mint backdrop and floor, no props, no horizon, no texture; even flat lighting, no shadows cast on the wall; camera locked off on a tripod at the worm's own eye level, centred medium shot, vertical 9:16, absolutely no camera movement, no zoom; cartoon, clean vector look; silent, no audio, no music, no captions`

Shot 1 action: `it wiggles in place, then lifts one flipper and tips its top hat toward the viewer`
Shot 2 action: `it wobbles side to side, spins one full turn around and bows low toward the camera`
Shot 3 action: `it finishes with one more full spin and claps its two flippers together`

**2. Cost and budget check**
- Quote (from the last successful `productions.quote`): 3 × $1.404 + $0.10 assembly = **$4.312**, 2156 credits, expected 15.501s.
- Your ceiling is $4.32 → **passes by 0.8¢.** There is no headroom: any edit that adds a shot, a keyframe or remaster breaks the cap. Leave `maxCredits` at exactly 2156 so an overspend is refused before anything renders.
- **Blocker A — funds.** The last balance reading was **1057.181 credits ≈ $2.11**, roughly **1099 credits (~$2.20) short** of the 2156 needed. As of that reading the render would be refused. I could not re-check the balance here, so treat it as stale but unconfirmed.
- **Blocker B — an identical production already failed.** `prod_c33e57a20a1af7094ce003d13093887a` (same 3-shot silent plan, maxCredits 2156) ended `status: failed` with `shots: []` and no `finishedAt`. Per the billing note a failed generation is refunded by Managed Media, so that attempt should have cost $0 — worth confirming on the credit ledger. The spec above is the retry, unchanged in cost but with the consistency wording made explicit.

**3. What to check the moment it runs** (cannot be done from here)
1. Poll the production to `status: succeeded` with a non-null `finishedAt` and three populated `shots`; assembly fee should settle as `$0.10` (total charged $4.312).
2. Confirm three clips in shotIndex order 0→1→2, ~15.5s total (H3 returns slightly over the 5s asked — expected ~15.501s, so trim nothing).
3. Confirm the delivered file is 1080×1920 (9:16) and has **no audio stream at all** (silent track, not just muted) by probing the media; confirm it plays 0→end with no freeze or gap at either join.
4. Then send me the shareable link plus actual dollars charged, and I'll record both in the series log.

**Not confirmed by me:** current credit balance, whether a top-up has happened, and therefore whether the render can launch at all. If text-mode H3 Max keeps failing, the guide's fix (frame modes for multi-shot stories) needs a different model id, which would violate the "MiniMax H3 Max for every shot" rule — that trade-off is the owner's call, not something to change silently.

**Left for the owner:** top up to at least 2156 credits (add ~1099 credits / ~$2.20) and submit the spec above with maxCredits 2156; then hand back the link so I can verify the silent full-length playthrough.
