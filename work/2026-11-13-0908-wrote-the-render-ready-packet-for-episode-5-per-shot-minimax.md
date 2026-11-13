# Wrote the render-ready packet for Episode 5: per-shot MiniMax H3 Max prompts, negatives, settings, assembly spec and QA list; flagged the 988.7-credit shortfall against the 1454-credit quote.

**Done**

2026-11-13 09:08 UTC, spent $0.03

- https://hivemindos.app/bee/104

**Episode 5 — The Worm's Wobbly Waltz, render-ready production packet (draft).**

**Confirmed from the quote already obtained (1454 credits)**
- 2 shots on minimax-h3-max-text-to-video at $1.404 each = $2.808, plus studio-assembly $0.10 = $2.908 total = 1454 credits (max 1500). Implied rate: 500 credits = $1, so each shot is 702 credits and assembly is 50.
- Expected runtime 10.334s, consistent with 2 × 5s shots.
- **Balance at quote time: 465.299 credits.** The quoted 1454 credits is 988.7 credits above the wallet. The quote's withinBudget flag compares against maxCredits (1500), not the balance, so the job still cannot be submitted as-is. This is the one blocker.

**Not confirmed / not done:** I have no render call available in this step and no video file exists. Nothing below has been executed; it is a packet ready to run. Exact Studio create-call argument names are unverified, so I have not invented them.

**Shot 1 — prompt (5.0s, vertical 9:16, 1080x1920)**
Vertical 9:16 cartoon animation, 5 seconds, single continuous take, locked-off camera at worm eye level, no cuts. A cheerful red cartoon worm - soft matte red body, big white googly eyes with black pupils that jiggle, a small black top hat perched on its head - performs a rhythmic, exaggerated, wobbly waltz-shuffle dance on a simple festive stage. The stage is a single wooden crate as the platform, rich red velvet curtains hanging behind, warm amber stage light from upper left, a soft shadow under the worm, plain dark backdrop. The worm bends into a C shape, compresses and stretches, hops on the beat, tail flicks; the body bounces comically and the googly eyes jiggle on every bounce. Style: 2D-style cartoon with soft 3D shading, saturated red, clean simple shapes. No text, no captions, no watermark. Ends mid-wobble with the worm upright and centered, framing and lighting identical to the opening frame.

**Shot 2 — prompt (5.0s, vertical 9:16, 1080x1920)**
Vertical 9:16 cartoon animation, 5 seconds, single continuous take, locked-off camera at worm eye level, no cuts, identical character, stage, framing, lighting and colour palette as the previous shot: a red cartoon worm with big googly eyes and a small black top hat on a wooden crate stage with red velvet curtains behind, warm amber light. Action: the worm stops dancing, plants itself centre-frame, then reaches up with its body tip, grips the brim of the top hat and tips it dramatically forward and down in a slow showman bow-tip, holding for a beat, then gives one enthusiastic bob upward so the top hat tilts off-kilter to one side and stays tilted. The worm holds that final pose, eyes wide, tail still, for the last half second so the shot ends freeze-friendly. No camera move, no text, no captions.

**Shared negative prompt:** extra limbs, human hands or arms, photorealistic worm, multiple worms, duplicated hats, sudden cuts, camera shake, zoom, on-screen text, captions, subtitles, watermark, logo, deformed or detached eyes, colour flicker, morphing, scene change, background characters.

**Settings:** model minimax-h3-max-text-to-video; aspect 9:16; 1080x1920; 5s per shot; same style tokens in both prompts (above) for character match; if the model exposes a seed, use one fixed seed for both shots; moderate motion strength; no audio generated.

**Fallback if Shot 1 is taken as a single 10s shot instead of 2 x 5s:** add loop the dance for the full duration, two complete wobble cycles, keep the same opening and closing framing. That changes the line items, so it needs a fresh quote before submitting - I have not assumed a price for it.

**Assembly:** studio-assembly, order shot0 then shot1, 9:16 1080x1920, hard cut at the 5s mark (the shared framing makes the seam invisible). Only add a short crossfade if the seam pops, which costs another assembly charge (50 credits per the quote's rate). Music is not part of either shot; whether the assembly step accepts an attached audio track is unconfirmed and I will check before submitting.

**QA checklist after render:** both eyes visible throughout; hat stays on head until the deliberate tilt; framing and colour match across the cut; no text or watermark; each shot 5.0s within about 0.2s; final pose held to the last frame.

**Left for the owner:** top up from 465.299 to at least 1454 credits (shortfall 988.7) and approve submitting the quoted 1454-credit job. Once that approval is in, the next check-in submits the two shots with the prompts above and assembles them.
