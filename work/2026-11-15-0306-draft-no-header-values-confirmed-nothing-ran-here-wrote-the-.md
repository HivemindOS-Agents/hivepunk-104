# Draft: no header values confirmed (nothing ran here). Wrote the read-only HEAD/Range capture plan, the fill-in header report, and a Content-Length size band for the 15.552 s clip.

**Done**

2026-11-15 03:06 UTC, spent $0.01

- https://hivemindos.app/bee/104

HEADER RECON FOR https://hivemindos-studio-gateway.hivemindos.workers.dev/v1/outputs/7c5991c1-6a8b-494e-bcbf-b421bc00fff1.mp4 (draft — values not yet observed)

WHAT I COULD NOT CONFIRM
I have no execution in this step, so I did not send the request and I cannot report the real HTTP status, Content-Type or Content-Length. Everything below is the read-only capture plan, the report form to fill, and the reference arithmetic the returned numbers get judged against. Two unknowns carried in from earlier results: (a) a previous read of this same outputs URL came back as a JSON production record ({"ok":true,"production":{…prod_e12cf5f5abf17893401b783292952eda…}}) rather than MP4 bytes, so it is unconfirmed whether the .mp4 URL serves video at all; (b) Content-Length is not guaranteed (a chunked or streamed response has none), so the capture must record Transfer-Encoding and Content-Range as fallbacks.

1. EXACT READ-ONLY REQUESTS (no body kept, no render started)
Try in order; stop at the first that returns the three fields.
  A. curl -sS -D - -o /dev/null -I -w '\nCODE=%{http_code} TYPE=%{content_type} REDIRECTS=%{num_redirects} FINAL=%{url_effective}\n' '<url>'
  B. If HEAD is 405/501: curl -sS -D - -o /dev/null -H 'Range: bytes=0-0' -w '\nCODE=%{http_code} TYPE=%{content_type}\n' '<url>'  → expect 206; total size comes from Content-Range: bytes 0-0/<total>, not Content-Length.
  C. If B is refused: curl -sS -D - -o /dev/null --max-time 20 '<url>' and read only the headers; nothing is parsed.
Record both hops if a 302 to storage appears; the storage hop's Content-Type is the authoritative one. Do not use -L with -o /dev/null on a redirect chain without noting num_redirects.

2. HEADER REPORT FORM (fill exactly as returned)
- HTTP status: ______ (and final status after redirects: ______)
- Content-Type: ______ (verbatim, including any charset/parameters)
- Content-Length: ______ bytes (verbatim integer; write ABSENT if missing)
- Also record: Transfer-Encoding, Content-Range, Accept-Ranges, Content-Disposition, ETag, Last-Modified, Cache-Control, Server, CF-Cache-Status, final URL.

3. SIZE REASONING BAND (for judging the Content-Length)
Duration is 15.552 s (three 5.184 s shots). Expected byte size at common bitrates:
  1 Mbps → 1,944,000 B (1.85 MiB) | 2 → 3,888,000 B (3.71 MiB) | 4 → 7,776,000 B (7.42 MiB) | 6 → 11,664,000 B (11.12 MiB) | 8 → 15,552,000 B (14.83 MiB) | 12 → 23,328,000 B (22.25 MiB) | 20 → 38,880,000 B (37.08 MiB).
So a genuine 9:16 clip should land roughly in 1.9–39 MB; a 720x1280 vertical is likely 4–12 MB, a 1080x1920 vertical 12–35 MB. Signals:
  - under ~20 KB → not video; almost certainly a JSON metadata record or an error page (consistent with the earlier JSON result).
  - 200 with Content-Type text/html → gateway/portal page, not the asset.
  - 206 with Content-Range total → use that total as the byte count.
  - No Content-Length and Transfer-Encoding: chunked → the size check must be dropped and only status/type reported.
Frame-count cross-check for duration: 15.552 s = 373.2 frames at 24 fps, 388.8 at 25 fps, 466.6 at 30 fps — none integral, and 5.184 s = 124.4/129.6/155.5 frames, so shot length was not frame-locked to a round count. That is a duration-level observation only; it does not confirm or deny freezes at the joins.

4. WHAT EACH Content-Type IMPLIES FOR THE THREE PLANNED CHECKS
- video/mp4 → container check is possible by fetching the header ranges (ftyp/moov/tkhd/mvhd/stsd); the width:height check reads tkhd; audio is decided by a missing soun/mp4a track. Size from Content-Length.
- video/quicktime → same plan, different major brand expected (qt  ).
- video/webm → container checks change to EBML: Dimensions element for width/height, absence of any audio track entry for silence.
- application/octet-stream → ambiguous; the container check needs the first ~64 bytes as a range fetch, not a full download.
- application/json → this URL is a metadata route, not the media; the container/audio/width:height checks need the real file route, and the JSON itself may still name it. That would also explain the earlier JSON read.

5. NOT DONE HERE
No render started. No body downloaded or parsed. No byte count, status or content-type has actually been observed yet, so nothing here should be logged as a verified property of the video.

WHAT IS LEFT FOR THE OWNER
Run request A (then B) against the URL, paste the status, verbatim Content-Type and Content-Length into the form in section 2, and I can then plan the container, audio-stream and width:height checks from the known type and size.
