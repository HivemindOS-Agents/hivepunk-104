# Drafted the productions.quote request for Episode 7 (one 9:16 image shot, 1.5s, model sound, captions on) from the studio guide rules; quote figure not confirmed.

**Done**

2026-11-09 00:56 UTC, spent $0.08

- https://hivemindos.app/bee/104

Draft of this step's work: the productions.quote request for 'Top Hat Worm Dance: Episode 7', built from the studio guide's rules (v1.0.1, minimax-h3-video-prompting 2.3.0) already recorded in the history. Nothing has been quoted, created or spent from this step.

Guide rules applied:
- Quote first, then set maxCredits at or above the quote on any create; a production that would spend more is refused before rendering.
- A single shot with one start frame uses mode 'image'.
- Keyframes are drawn at the production's aspect; the start frame is 9:16, so it fits.
- Captions are timed on the finished cut, and H3 shots run slightly longer than requested, so caption timing should use expected lengths, not 1.5s.
- sound 'model' keeps the models' own audio and is the cheapest paid lane.
- Aspect stays 9:16 for social posts.

Exact quote request to send (productions.quote only, no maxCredits, no characters, no end frame):

{
 "action": "productions.quote",
 "production": {
 "title": "Top Hat Worm Dance: Episode 7",
 "aspect": "9:16",
 "sound": "model",
 "captions": true,
 "shots": [
 {
 "index": 1,
 "mode": "image",
 "duration": 1.5,
 "startImageUrl": "https://hivemindos-paid-agent-gateway.hivemindos.workers.dev/api/media/managed/outputs/8c85f19b-08fa-4859-ba33-ee814202ee3f.jpeg",
 "prompt": "A stout cartoon red worm wearing a black top hat wiggles its whole body in a silly dance and tips its hat. Locked wide master at the worm's own eye level, one action, plain empty room, crisp neutral daylight, short shadows, no orange or golden tint anywhere."
 }
 ]
 }
}

What I could not confirm: the quote figure. Quotes are priced server-side and I cannot run one from this step, so I have not stated a credit cost. The start image URL is the one recorded in earlier steps; I have not verified it resolves.

Left for the owner: run this quote against the Hivemind Studio service and return the credit figure, and confirm the start image URL is live. Only then can a productions.create be sent with maxCredits set to the agreed ceiling.
