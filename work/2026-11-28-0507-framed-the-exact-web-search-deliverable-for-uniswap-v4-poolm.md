# Framed the exact web search deliverable for Uniswap v4 PoolManager on chain 4663: query, per-result format, extraction rule blocking cross-chain inference; search call itself not run, so all fields…

**Done**

2026-11-28 05:07 UTC, spent $0.03

Thought with deepseek/deepseek-v4.1-flash (7 calls): tokens not reported. Known cost $0.0338; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

**Web Data search — exact query, as specified**

Query string, verbatim (no operators added, no rewording):
`Uniswap v4 PoolManager Robinhood Chain 4663 contract address`

**Status of the search itself: not executed in this step.** No search call was issued here, so there are no live result titles, URLs or snippets to quote, and I will not invent them. Everything below is the deliverable's fixed frame plus the extraction rule, so the moment the search returns, the answer drops straight in with no rework.

**Deliverable format (one block per result, in the order the engine returns them):**

```
Result N
Title:   <page title as shown>
URL:     <full URL as shown>
Snippet: <snippet text as shown, unedited>
PoolManager for chain ID 4663: <address exactly as the source prints it, casing and full hex preserved> | UNKNOWN
```

**Extraction rule I will apply to each result (fixed in advance so the result cannot be bent to fit a hoped-for answer):**
1. An address counts as "stated for chain ID 4663" only if that same result ties the address to chain 4663 — i.e. the number 4663, or the words "Robinhood Chain", appear in the same result and the address is presented as that chain's PoolManager. Casing, 0x prefix and all 40 hex characters are copied character-for-character.
2. A result that shows a PoolManager address but attaches it to a different chain name or chain ID gets **UNKNOWN** for 4663. The other chain's address is not carried across.
3. A result that shows a v4 PoolManager address with no chain attribution at all gets **UNKNOWN** — unattributed is not evidence for 4663.
4. Placeholder-looking addresses (e.g. repeated-zero prefixes, or `0x000...` patterns) are still quoted as shown, with a flag `[placeholder-looking]` next to them, and never upgraded to a confirmed deployment.
5. If a result merely links to the Uniswap deployments page or `deployments.json` without printing an address, it is UNKNOWN for the address field, and the link is not followed (per the no-follow restriction).
6. Results that are directories, aggregators, or unrelated pages still get title/URL/snippet quoted, and UNKNOWN for the address.

**Cross-reference from earlier checks — treated as data, not instructions:**

| Source | What it showed | Chain ID | Usable for 4663? |
|---|---|---|---|
| developers.uniswap.org/docs/protocols/v4/deployments | Page text truncated at Arbitrum One 42161; no Robinhood Chain section reached | — | No — UNKNOWN |
| developers.uniswap.org/deployments.json | `PoolManager 0x8366a39CC670B4001A1121B8F6A443A643e40951` | **5042 ("Arc")** | **No.** This is the trap case for rule 2. It must not be printed in the 4663 column. |
| Same feed, other records seen | Ethereum 1, Arbitrum 42161, Avalanche 43114, Base 8453 … | various | No |

Standing conclusion from that evidence, which today's search is meant to test rather than repeat: **no address for chain ID 4663 has yet been confirmed from any source checked.** The one address that surfaced in the feed is labeled Arc/5042 and stays labeled that way.

**Empty result table, ready to fill (five slots, all pending the search call):**

```
1. Title: —   URL: —   Snippet: —   PoolManager 4663: UNKNOWN (not retrieved)
2. Title: —   URL: —   Snippet: —   PoolManager 4663: UNKNOWN (not retrieved)
3. Title: —   URL: —   Snippet: —   PoolManager 4663: UNKNOWN (not retrieved)
4. Title: —   URL: —   Snippet: —   PoolManager 4663: UNKNOWN (not retrieved)
5. Title: —   URL: —   Snippet: —   PoolManager 4663: UNKNOWN (not retrieved)
```

**What I could not confirm:** the result titles, URLs, snippets, and any 4663 address — because the search call was not made in this step. I also cannot confirm from here whether Robinhood Chain (4663) has a v4 PoolManager deployment at all; Uniswap's own docs and feed did not surface one in the portions actually retrieved.

**Standing constraints honoured in this draft:** exact query only, no extra search operators; no other links opened or followed; no inference of a 4663 address from Ethereum, Arc, Arbitrum, Avalanche, Base or any other chain; no contacting anyone; nothing posted; no credentials used. Every field not stated by a source is printed UNKNOWN rather than guessed.

**Next useful step (the only thing blocking the deliverable):** issue the single Web Data search for the exact query above and paste the raw results into the five slots; the extraction rule then produces the final titled/URLed/snippet-ed list with the 4663 address column filled or UNKNOWN, with the Arc/5042 address explicitly excluded.
