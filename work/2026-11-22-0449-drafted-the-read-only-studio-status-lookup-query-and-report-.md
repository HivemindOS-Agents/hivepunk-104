# Drafted the read-only Studio status-lookup query and report form for episode 20; evidence points to quote-only, never started, no 2156 charge, but the job record itself remains unconfirmed.

**Done**

2026-11-22 04:49 UTC, spent $0.03

Thought with deepseek/deepseek-v4.1-flash (9 calls): tokens not reported. Known cost $0.0333; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

## Read-only status lookup — 'Worm dance, episode 20 — vertical, native sound'

**What I could not do:** I have no Hivemind Studio tool in this step, so I could not open the job list or the job record itself. Everything below is built from the three Studio quote responses already in my history; the studio-side lookup still has to be run. I did not start, restart, re-quote or re-render anything, and spent nothing.

### The exact read-only query to run (no spend, no job creation)

```
studio.listJobs({ limit: 20, order: "createdAt desc" })
→ find job.title === "Worm dance, episode 20 — vertical, native sound"
→ if found: studio.getJob(job.id)  // read-only: stage, shotIndex, error, videoUrl, durationSeconds, creditsCharged
→ also: studio.getBalance()       // compare to 2088.841 credits at quote time
→ also: studio.listCharges({ since: 2026-11-22T02:41, limit: 50 })  // any 2156 or partial debit
```
That is read-only by construction: list/get/balance only, no `createJob`, no `quote`, no `render`.

### Evidence already on hand about this job

| Time (epoch ms) | Request | What came back | Balance after |
|---|---|---|---|
| 1795311471363 | Episode 19 — quote and produce | quote only: 3×1.404 + 0.1 = 4.312 USD / 2156 credits, 15.501 s expected | 2098.999 |
| 1795315298812 | **Episode 20 — quote and produce** | **quote only: same 4 items, 4.312 USD / 2156 credits, 15.501 s; no job id, no video link, no stage field** | **2088.841** |
| 1795319142382 | Episode 21 — quote and produce | quote only: same 4 items, 4.312 USD / 2156 credits | 2079.347 |

Details for the episode 20 record specifically: shots 0/1/2 on `minimax-h3-max-text-to-video` at 1.404 USD each, plus one `studio-assembly` at 0.1 USD; `priceUsd` 4.312, `maximumUsd` 4.312, `priceCredits` 2156, `expectedSeconds` 15.501, way `fast`, ~5 min, `withinBudget: true` with `maxCredits: 3000`.

### What that lets me say about (a)–(d)

**(a) Current stage — not confirmable from here.** The episode 20 response object contains no `jobId`, no `status`, no `stage`, no `videoUrl`. Every field it does contain belongs to a quote. So I have no studio-side stage to report. My working hypothesis, to be checked by the query above: **the job was never started** — the "produce" call returned a priced quote and stopped there.

**(b) Final video link / duration / cost — nothing to report.** No link was ever returned for episode 20. Expected duration at quote was 15.501 s (3 × 5 s plus assembly), expected cost 4.312 USD / 2156 credits; both are projections, not results.

**(c) Failure or stall text — none recorded.** No error string, no stopped-at stage exists in my history for this title, so there is nothing to quote verbatim. If the studio record shows `failed` or `stalled`, capture the stage and error as literal text; do not paraphrase.

**(d) Was 2156 credits or part of it charged? — Almost certainly not, on the balance evidence.** Balance went 2098.999 → 2088.841 → 2079.347 across the three quotes, i.e. small movements of 10.158 and 9.494 credits. A 2156-credit debit would have dropped the balance to about 2088.841 − 2156 = **−67.159 credits**, which is not what the next quote saw (2079.347, positive, and only 9.494 lower than expected). So no full charge and no visible partial charge tied to this job. Those 9–10 credit steps are unexplained by anything in my history and are worth identifying in `listCharges` — they are two orders of magnitude too small for a shot render on this model, so they are more likely per-call or unrelated activity. This is an inference from three balance readings, not a ledger read.

**Balance note worth flagging to the owner:** at 2088.841 credits the balance was already **67.159 credits short** of the 2156-credit quote, even though the quote itself reported `withinBudget: true` (that flag was measuring against `maxCredits: 3000`, not against the balance). Any attempt to actually start this job would have had to fail on funds, or draw on something other than the visible balance.

### Most recent jobs I can see, by title and status

I can see none — my history holds quote objects, not a job list, so I cannot yet tell you whether episode 20 was never started. The three titles I know were *quoted* are:

1. `Worm dance, episode 19 — vertical, native sound` — quoted, 2156 credits, no job record seen
2. `Worm dance, episode 20 — vertical, native sound` — quoted, 2156 credits, no job record seen
3. `Worm dance, episode 21 — vertical, native sound` — quoted, 2156 credits, no job record seen

If `listJobs` returns nothing matching these titles, the correct conclusion is that all three were quoted and never launched, and the consistent quote-only response shape across 19, 20 and 21 supports that reading.

### Report form, ready to fill once the lookup runs

```
Title: Worm dance, episode 20 — vertical, native sound
Job id: <from listJobs, or "none — title absent">
(a) Stage: queued | rendering shot N of 3 | assembling | finished | failed | stalled
(b) If finished: videoUrl=<...>  durationSeconds=<...>  creditsCharged=<...>
(c) If failed/stalled: stoppedAt=<...>  errorText="<verbatim>"
(d) Charge taken: full 2156 | partial <n> | none — balanceBefore=2088.841 balanceNow=<...> chargeId=<...>
Other recent jobs: <exact titles + statuses, newest first>
```

**Left for the owner:** run the four read-only Studio calls above (listJobs, getJob, getBalance, listCharges) and paste the results into the form — that is the only missing piece, and it costs nothing.
