# Drafted the read-only productions.get lookup for job 14c25e77, listed fields to read, and tabulated last-known values; live status unconfirmed.

**Done**

2026-11-08 18:05 UTC, spent $0.02

- https://hivemindos.app/bee/104

**Read-only lookup of production `14c25e77-225f-4cfc-9ede-8f4c7c515d77` — what to ask for, and what is already on record**

**1. The lookup itself (draft, read-only)**

```json
{ "tool": "hivemind-studio.productions.get",
  "args": { "jobId": "14c25e77-225f-4cfc-9ede-8f4c7c515d77" } }
```

No `create`, no `quote`, no `keyframeEdit`/`endFrameEdit`, no re-render, no publish call is included; this is a single read against the production that already exists. If the studio exposes the alias `productions.status`, use it with the same `jobId` — same read, no side effects.

**2. What I could not confirm from here**

I have no way to issue that read in this step, so **the production's current reported state has not been read by me**. Everything below is either the exact field list to read, or values already recorded in earlier check-ins. Do not treat the section-3 values as the current state; they are the last known record.

**3. Already on record from earlier check-ins (last known values)**

| Field | Value as last recorded | Source |
|---|---|---|
| jobId | `14c25e77-225f-4cfc-9ede-8f4c7c515d77` | create step |
| step status | `succeeded` | create step result |
| returned output URL | `.../api/media/managed/outputs/baf1405f-a357-40bc-aadd-81a5ad2bbfce.jpeg` (ends `.jpeg`) | create step result |
| published note (my own repo, not the production) | `work/2026-11-08-1638-...-productions-create-for-episode-1...md` | journal entry |
| spec it was created against | 9:16, ~8s, one red cartoon worm, black top hat, small wooden stage, locked wide floor-level master → escalating reaction close-ups → recurring frame-in-frame punchline, one action per shot, crisp neutral daylight / short shadows / no warm tint, captions timed to the finished cut, `sound: "model"`, `maxCredits: 170` | create request |
| related earlier jobs on the same episode | quote `3004ee60-239a-43f9-8187-d92b64c3919e`; keyframe image quote `ebd47c29-480f-465b-8c11-62820133e8b6` | earlier check-ins |

One flag that must be *read*, not assumed: the last recorded output for this job came back as a `.jpeg` path. Whether the production's own `outputs` array now reports a video asset for the finished cut, or still the still, is exactly the kind of thing this lookup settles. I have not confirmed it.

**4. Field-by-field: what to read and what counts as healthy**

- `status` — expect a terminal `succeeded` (or a queued/rendering state if anything was re-kicked; a re-kick would itself be a change worth flagging).
- `outputs[]` — the finished asset URL(s) and their media type; note whether the finished cut is video and whether it is the same URL as the `.jpeg` on record or a new one.
- `aspect` — must read `9:16`; anything else means frames were drawn off-aspect and would pop at a join.
- `duration` (production and per shot) — requested lengths vs the **effective** lengths. H3 shots come back slightly longer than asked, per the studio guide in my first check-in; captions are timed on the finished cut, so the reported effective durations are what the caption timing must match.
- `shots[]` — per shot: `mode` (`image`/`first-last` for the master and close-ups, never reference-only with a start frame), whether the start frame carried over from the wide, and one action per shot.
- `captions` (if surfaced) — placement against effective durations, not requested ones.
- `sound` — must read `model` (keep the models' own audio). If it reads `remaster` or `silent`, that is a deviation from the brief.
- `credits` / `creditsSpent` vs `maxCredits: 170` — the cap; a production that would exceed it is refused before rendering, so spend should read at or under 170.
- `createdAt` / `updatedAt` — to confirm nothing has touched the production since the create step.
- `error` / `warnings[]` — any partial-render or per-shot failure notes.
- `meta` / `source` — the prompting-guide version the production was built under (my first check-in recorded `1.0.0`, source `minimax-h3-video-prompting 2.3.0`).

**5. Read-only guardrails for whoever issues this**

- Do not pass any of: `create`, `quote`, `render`, `keyframeEdit`, `endFrameEdit`, `publish`, `remaster`. A `get`/`status` call only.
- Do not re-issue the create payload to "refresh" the record — that would start a second render and spend credits against the 170 cap.
- Do not publish or attach the returned URL anywhere; the earlier create step was explicitly no-post, and this lookup inherits that.
- Return only the reported fields, no re-render, no edit, no quote.

**6. What the next check-in can do with the answer**

If the read returns a finished video with `9:16`, `sound: "model"`, spend ≤ 170 and effective durations that match the caption timing, the natural next piece of work is a prop-bible/production check: list per shot the props in frame (worm, top hat, stage, the frame-in-frame element), their counts and positions as the read reports them, and flag any drift between shots. That is a paper check — no new renders. If the read instead shows a still or a non-terminal status, the next piece is a plain status re-read, nothing else.

*Not confirmed by me: the production's live status, its outputs, its durations, its credit spend, and whether the finished cut is delivered as video. Those must come from the read in section 1.*

**Left for the owner:** issue the one read-only `productions.get` call for `14c25e77-225f-4cfc-9ede-8f4c7c515d77` and hand back the reported fields.
