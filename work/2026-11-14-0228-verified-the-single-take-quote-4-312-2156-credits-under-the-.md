# Verified the single-take quote: $4.312/2156 credits, under the $4.32 limit, but account balance is only 1023.561 credits — a 1132-credit shortfall that likely blocks the render; drafted the exact…

**Done**

2026-11-14 02:28 UTC, spent $0.05

- https://hivemindos.app/bee/104

# Worm dance, final — silent vertical: render readiness check (draft, not submitted)

## 1. What the last call established (quote only, no charge)
The single-take quote came back clean and matches the spec, so the pricing question is closed:

| Item | kind | model | price |
|---|---|---|---|
| 1 | shot 0 | minimax-h3-max-text-to-video | $4.212 (2106 credits) |
| 2 | assembly | studio-assembly | $0.10 (50 credits) |
| **Total** | | | **$4.312 / 2156 credits** |

- `expectedSeconds`: 15.083 (i.e. the ~15 s single continuous take you asked for).
- Rate implied: **2156 credits = $4.312 → exactly $0.002 per credit**, so ~139.6 credits per second of video at this model.
- Against your hard limit of $4.32: **passes, but only by $0.008 (0.19%)**. Any re-quote that adds seconds will break the limit.
- One correction worth recording: the quote **does** include a $0.10 `studio-assembly` fee even for a single generation with no splitting and no keyframes. "Single take" removes shot-splitting cost, not the assembly line item.

## 2. The blocking finding
Same quote payload reported `balanceCredits: 1023.561`.

- Cost of this render: **2156 credits.**
- Balance on hand: **1023.561 credits.**
- Shortfall: **1132.439 credits ≈ $2.265** — the account holds roughly **47% of what this render needs.**

This is the most useful thing found this check-in, because it also explains the two prior failures better than anything else on record. The failed "Worm dance, episode 2" production (id `prod_e6b254b7b0fd22e793220ad9c1ee9d4e`, then retry `prod_04b7bbf97935788fa653c1e3cfa5c9f0`, which queued successfully and then went to `failed` with no shot ever produced) carried **the identical 2156-credit price**. A queued-then-failed production with zero shots returned is consistent with the credit hold being rejected before any generation launched.

**What I cannot confirm from here:** the actual failure reason string. The job payload came back as a bare `"The job failed."` with no error code, and I have no account/ledger access in this step. Treat the credit shortfall as the leading hypothesis, not a proven cause — a model-side generation fault would look the same from outside. I am not claiming the prior jobs failed *for* insufficient credits; I am saying the shortfall is real, verified in the quote payload, and would by itself stop this render.

## 3. Ready-to-submit render request (draft — owner or build step must submit)
Every parameter below is exactly as specified, nothing guessed:

> **Title:** Worm dance, final — silent vertical
> **Mode:** text · **Model:** minimax-h3-max-text-to-video · **Shots:** 1 (single generation, no shot splitting, no keyframes) · **Seconds:** 15 · **Aspect:** 9:16 · **Sound:** silent (no audio, no music, no voiceover, no SFX) · **Captions:** none · **Camera:** locked and static, no movement
> **maxCredits:** 2156
> **Shot prompt (verbatim):** "A bright flat-color stage, evenly lit, with a small red cartoon worm with big round googly eyes wearing a black top hat; the camera holds perfectly still the whole time. In one continuous take the worm first tips its black top hat toward the viewer, then wobbles and spins once all the way around and bows low toward the camera, then finishes with a matching full spin and claps its flippers together. Silent, no audio."
> **Then:** read back the finished production and deliver the finished clip. Report complete only after the clip is delivered.

## 4. Options to clear the shortfall (numbers, for the owner to pick)
1. **Top up 1132.439+ credits (≈$2.27)** → submit §3 as-is. Cleanest; keeps your 15 s, 9:16, single-take, $4.312 spec intact and under the $4.32 limit.
2. **Shorten the single take to ~7 s.** Balance 1023.561 − 50 (assembly) = 973.561 credits ÷ 139.6 credits/s ≈ **6.97 s.** That is a real change to your spec, so I am *not* proposing it as a substitution — it is only the largest duration that fits today's balance.
3. **Split into two shots — does not help.** Assembly ($0.10) is charged once per production, and per-second shot pricing is unchanged, so splitting still totals ~2156 credits. Rule this one out.

## 5. Honest status
No render was submitted in this step and nothing was charged. The mission is **not** complete: the clip does not exist yet. Both prior attempts on the sibling production ended `failed`, and this render cannot proceed on the present balance. Nothing here has been run or tested; the request in §3 is a draft.

**Left for the owner:** add ~1132 credits (≈$2.27) to the account, or authorize the ~7 s shortened take, then submit the §3 request with `maxCredits: 2156` and read back the finished clip.
