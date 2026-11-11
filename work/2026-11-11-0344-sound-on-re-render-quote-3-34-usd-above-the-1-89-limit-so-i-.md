# Sound-on re-render quote: $3.34 USD, above the $1.89 limit, so I stopped without rendering or charging; base silent render was $2.3275.

**Done**

2026-11-11 03:44 UTC, spent $0.02

- https://hivemindos.app/bee/104

## Sound-on re-render quote — “Worm Disco Limbo Redux”

**Quoted price: $3.34 USD.**

That is above your $1.89 limit, so per your instruction I am giving the figure and stopping. No render started, no credits spent, nothing charged.

### Where the number comes from

| Item | Figure | Source in my records |
|---|---|---|
| Base render, as delivered (silent) | **$2.3275 USD / 1163.75 credits** (maxCredits 1163.75, settled) | Read-only status check on `prod_f631e03b7895d1d5585187f531133e28`, status `complete` |
| Same production, 3 shots, 15.125 s | 3 shots × 5.042 s, `audioPeak: null` (no audio track present) | Same status check |
| Sound-on re-run quote | **$3.34 USD (≈1670 credits)** | Prior check-in against the $1.90 remaining budget |
| Implied cost of adding audio | ≈ **+$1.01** over the silent render | Difference of the two |
| Budget at the time | $1.90 remaining that day — the quote is ~1.8× over | Prior check-in |

Credit-to-USD rate implied by the production record: 1163.75 credits = $2.3275, i.e. $0.002 per credit (500 credits ≈ $1.00). At that rate $3.34 ≈ 1670 credits.

### What the $3.34 does and does not cover
- Covers: re-rendering all three shots from the same shot plan and reference stills, same 15.125 s total length, with an audio track included in the output.
- Does not cover: any change to visuals, length, or shot count; and it is priced as *new shot generations*, not as adding an audio stream to the MP4 you already have.
- Worth asking the studio about, but **not quoted and I cannot price it from here**: a remux/audio-add pass that keeps the existing finished visuals untouched and only muxes in an AAC track. That path would avoid re-generating shots and should be well under the $3.34 figure. No such price has ever been quoted to me.

### Plainly not confirmed
- I did **not** pull a fresh quote in this step. The $3.34 is carried forward from my previous check-in, not re-fetched just now, so I cannot independently re-verify it at this moment.
- I could not confirm whether the studio exposes a cheaper “keep existing visuals + add audio” service at all.
- I could not confirm the audio format it would emit (the X-upload guidance from my earlier research points to AAC LC in MP4).

### Owner decision left
1. Confirm at **$3.34** and release the budget for a full sound-on re-render, or
2. Have me ask for a remux-only (no re-generation) audio-add quote first — likely cheaper, unquoted today, or
3. Leave the video silent.
