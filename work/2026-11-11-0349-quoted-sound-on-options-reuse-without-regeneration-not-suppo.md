# Quoted sound-on options: reuse-without-regeneration not supported/quotable; only price is full re-render $3.34 / ~1,670 credits; audio format unconfirmed. No render, no spend.

**Done**

2026-11-11 03:49 UTC, spent $0.05

- https://hivemindos.app/bee/104

## Quote only — sound-on assembly for prod_f631e03b7895d1d5585187f531133e28 (Worm Disco Limbo Redux)

**Nothing was rendered, no credits were spent, nothing was charged.** Every option below exceeds the $1.89 remaining daily limit, so this stays a quote.

### Answer first

1. **Reuse-without-regeneration (existing three shot videos unchanged + audio added): not supported as far as I can confirm.** Nothing in the production record, and no capability available to me, exposes a remux or audio-add pass. The only sound-on price I have ever been given is for a *full re-render* of the shots. So I cannot give you a price for this path, because none exists to quote — it is not a matter of it being expensive, it is that the service is not visible to me.
2. **The only path I can actually price** — re-rendering the same three shots at the same 15.125 s with an audio track — is **$3.34 USD / approximately 1,670 credits**.
3. **Audio format: not confirmed for Studio.** X's own upload guidance points to MP4 with AAC LC audio (mono or stereo). I cannot state that the studio emits that.

### The production's known facts (from the read-only status check)

| Field | Value |
|---|---|
| Status | complete, finished 2026-11-10T09:46:41Z |
| Shots | 3, all complete, 5.042 s each |
| Total duration | 15.125 s |
| Silent render, as delivered | $2.3275 USD / 1,163.75 credits, maximumCredits 1,163.75, assembly fee settled |
| Audio in delivered file | `audioPeak: null` — no usable audio track |
| Implied credit rate | 1,163.75 credits = $2.3275, i.e. **$0.002 per credit** (500 credits = $1.00) |

Note: your earlier brief mentioned a 1,400-credit cap, but the production record itself reports maximumCredits of 1,163.75. I could not resolve that discrepancy, and it matters, because a 1,670-credit sound-on job would exceed either cap and would need a new production or a raised ceiling.

### Itemised price — full sound-on re-render (the only quotable path)

Derived from two figures I hold: the settled silent render ($2.3275 / 1,163.75 credits) and the sound-on quote ($3.34). The split below is **implied by subtraction, not a fresh line-item quote**.

| Line item | Credits | USD |
|---|---|---|
| Video generation, 3 shots x 5.042 s (already paid once on the silent run) | 1,163.75 | $2.3275 |
| Audio, implied = $3.34 minus $2.3275 | ~506.25 | ~$1.0125 |
| Assembly fee | settled / re-charged once at delivery — whether it re-charges on a second delivery is **not confirmed** | — |
| **Total, sound-on re-render** | **~1,670** | **$3.34** |

Per-shot implied audio cost: ~168.75 credits (~$0.34) x 3.

### Itemised price — reuse-without-regeneration (the thing you actually asked for)

| Line item | Credits | USD |
|---|---|---|
| Re-generating the three existing shots | 0 (unchanged) | $0.00 |
| Reusing existing shot videos | **not offered / not confirmable** | — |
| Audio track creation | **not quoted** | — |
| Remux / assemble | **not quoted** | — |
| **Total** | **no quote available** | **no quote available** |

I deliberately give no invented number here. If the studio does offer this, it should be well under $3.34, because the dominant line — 1,163.75 credits of shot generation — disappears entirely. But I have never been quoted it, and I will not present an estimate as a price.

### Cheapest sound-on alternatives, ranked

1. **Add audio outside Studio — $0.00 in Studio credits.** Take the existing finished MP4 (`9e3755e1-...mp4`, 15.125 s) and mux an AAC LC stereo track into the container yourself or with any free editor. The visuals are untouched, no shot generation, no Studio charge. This is the genuinely cheapest sound-on path and it produces the format X wants. Caveat: it is not a Hivemind Studio deliverable, and the studio copy stays silent.
2. **Single-shot sound-on render — estimated ~$1.11 / ~557 credits (derived, NOT quoted).** If the audio line scales with shot count, one 5.042 s sound-on shot is roughly a third of $3.34. That is my arithmetic from the same two figures, not a price anyone gave me. It would also be a different video (one shot, not three).
3. **Full sound-on re-render — $3.34 / ~1,670 credits.** The only real quote. Same visuals, same 15.125 s, audio included, but it re-generates all three shots and re-charges them.

### Plainly not confirmed
- I did **not** pull a fresh quote in this step. $3.34 is carried forward from my 2026-11-11 check-in, not re-fetched now.
- Whether any remux / audio-add-only service exists: **unconfirmed either way**.
- Whether the assembly fee re-charges on a second delivery of the same production.
- The exact audio codec, sample rate, channel layout, or bitrate the studio would emit. Best available target: MP4 container, AAC LC, stereo.
- The maximumCredits figure (1,163.75 vs the 1,400 you mentioned).

### Left for the owner
Either (a) approve $3.34 / ~1,670 credits for a full sound-on re-render, (b) have me request a reuse-without-regeneration quote from the studio directly, since I cannot see one, or (c) take the $0.00 route and mux audio into the existing MP4 outside Studio. Nothing starts until you say which.
