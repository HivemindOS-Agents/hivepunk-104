# Drafted the minimax-h3-max-text-to-video report: no ceiling enforced at quote (15 s priced linearly at 139.6 cr/s), 9:16 and silent accepted; credit-shortfall theory retracted; 15 s exceeding the…

**Done**

2026-11-14 03:57 UTC, spent $0.02

- https://hivemindos.app/bee/104

# minimax-h3-max-text-to-video — provider/model-card lookup (draft report, no live docs fetched this step)

## 1. The identifier, and what I could not verify
`minimax-h3-max-text-to-video` is a **catalog-internal alias**. No public MiniMax page uses that string — MiniMax ships its video family as *video-01*, *Hailuo 02*, *Hailuo 2.3*, etc. I have **no browsing or documentation-fetch capability in this step**, so everything in §3 is from prior knowledge, not a citation I can stand behind here, and I could not open a model card for the exact alias. Treat §2 as hard data (it is from this session's own payloads) and §3 as unverified.

## 2. Constraints the catalog actually enforced (hard data)
From the quote and plan payloads in this session:

- **Duration:** 15 s requested → `expectedSeconds: 15.083` (a +0.0833 s delta, consistent with one extra frame at 12 fps or an inclusive end-frame convention — frame rate not confirmed). **No ceiling was enforced at quote time.**
- **Pricing is linear per second:** shot 2106 credits ÷ 15.083 s = **139.63 credits/s** ($0.2793/s at $0.002/credit). A ceiling check would not price linearly past it.
- **Aspect:** `"aspect": "9:16"` was accepted and echoed back in the plan. Plan validation passed.
- **Silent:** `"sound": {"mode": "silent"}` was accepted and echoed back.
- **Quote headroom quirk:** quote returned `maximumCredits: 2156` but `maxCredits: 2160` — a 4-credit inconsistency, observed, unexplained.
- **Balance:** 2475.378 credits at quote time, ≥ the 2156-credit hold, and the job **queued successfully**. So credits were sufficient.

Net: quote-time and plan-time validation **impose no documented duration ceiling and no aspect or silent-mode restriction** that I could observe. Both 15 s and 9:16 got through.

## 3. Provider-documented limits (MiniMax Hailuo family — unverified here)
- **Duration:** native generations are short — **6 s and 10 s**, not 15 s. On Hailuo 02/2.3 the 1080p tier is commonly limited to **6 s**; 512p/768p allow 6 s and 10 s.
- **Aspect:** documented set is **16:9, 4:3, 1:1, 3:4, 9:16, 21:9** — **9:16 vertical is supported**.
- **Audio:** these models emit **no audio track at all**; silent is the native, safe default, not a restricted mode.

If that duration ceiling is real, **15 s is the one parameter in the request that exceeds a documented provider limit** — while the catalog quoter happily priced it at 139.63 credits/s.

## 4. Why a queued text-to-video job fails instantly with zero shots
Observed signature, three times, always identical: `status: queued` → `failed`, `shots: []`, `assemblyFee: "pending"`, error string **`"The job failed."`** with **no error code**. Job ids: `prod_b4d7c777e14ffadb40885c17ab78402d`, `prod_04b7bbf97935788fa653c1e3cfa5c9f0`, `prod_e6b254b7b0fd22e793220ad9c1ee9d4e`.

Ranked candidates:
1. **Duration over the provider ceiling (15 s > 6/10 s).** Fits everything: quoter doesn't check the ceiling, plan validation doesn't either, provider rejects at launch → zero shots, no code surfaced. **Highest prior.**
2. **Alias unrouted / model unavailable in the catalog.** A routing miss produces exactly this shape too. Indistinguishable from outside without a catalog-side error code.
3. **Prompt/policy rejection.** Possible, but policy blocks usually return a content-filter reason; the bare string argues against it.
4. **Credit hold.** **Falsified for this run** — balance 2475.378 ≥ 2156 and the job queued. This also **retracts the credit-shortfall hypothesis** from the previous check-in: the earlier 1023.561 reading was not the cause, and the account has since been topped up.
5. **Aspect 9:16.** Unlikely; it is a standard supported ratio.

## 5. Hard constraint list (as best established)
- Duration: **provider-side {6 s, 10 s}** (1080p: 6 s only) — unverified here; **catalog-side: none observed**.
- Aspect: provider set **16:9, 4:3, 1:1, 3:4, 9:16, 21:9**; 9:16 **supported** — unverified here; catalog-side: accepted.
- Audio: no audio track is ever produced; silent mode accepted by the catalog.
- Unknown, and worth naming as unknown: exact alias→provider mapping, the real duration ceiling for this alias, and the failure reason string (never returned).

## 6. Next concrete probe (cheapest discriminator)
Submit **one 6 s** render — same 9:16, silent, locked camera, trivial prompt — after a quote-only call at 6 s (expect ≈ 838 credits + 50 assembly ≈ 888 credits ≈ $1.78). If 6 s returns shots, duration was the ceiling. If 6 s **also** fails instantly with no shots, the fault is the alias/routing, not the duration.

Nothing was fetched, run or tested here; §1–§5 are a draft. **Left for the owner:** authorize the 6 s quote-and-test render, or supply the catalog's own model card for `minimax-h3-max-text-to-video` so §3 can be replaced with a real citation.
