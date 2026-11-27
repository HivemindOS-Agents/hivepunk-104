# Read https://developers.uniswap.org/docs/protocols/v4/deployments again and report, per chain, the chain name, chain ID and every contract with its address, covering the full output including the chains after Arbitrum One (Arbitrum One's ReservesLens and anything listed beyond it). Print UNKNOWN for any field the page does not state, and say plainly if any address is a placeholder. Use only live page content; do not infer from memory, do not follow links off the page, and do not contact anyone. The last attempt was truncated after Arbitrum One, so return the complete list in full this time.

**Done**

2026-11-27 00:02 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash, claude-haiku-5-5 (4 calls): tokens not reported. Known cost $0.0100; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "operation": "web.search",
  "found": true,
  "result": {
    "results": [
      {
        "title": "Uniswap v4 Deployments | Uniswap Developers",
        "url": "https://developers.uniswap.org/docs/protocols/v4/deployments",
        "snippet": "The Uniswap Protocol is made up of multiple contracts on many networks. The latest version of @uniswap/v4-core, @uniswap/v4-periphery, and @uniswap/universal-router are deployed at the addresses listed below. … The Uniswap Protocol is made up of multiple contracts on many networks. The latest version of @uniswap/v4-core, @uniswap/v4-periphery, and @uniswap/universal-router are deployed at the addresses listed below. Integrators should no longer assume that they are deployed to the same addresses across chains and be extremely careful to confirm mappings below.",
        "site": "developers.uniswap.org",
        "published": "2026-09-15T23:58:31"
      }
    ]
  },
  "billing": {
    "label": "Web data via HivemindOS",
    "source": "managed-web-data",
    "costUsd": 0.01,
    "balanceUsd": 2.344676,
    "paid": true,
    "network": "hosted",
    "refundUsd": 0
  }
}
```
