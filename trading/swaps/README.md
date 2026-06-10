---
description: Market buy or market sell any supported SPL token.
icon: arrow-right-arrow-left
---

# Swaps

Swaps are **market orders** — they execute instantly at the best available route. For price-triggered trades, see [Limit Orders](../limit-orders.md).

### Before you swap

* You need a wallet ([Setting Up Your Wallet](../../overview/getting-started/setting-up-your-wallet.md)).
* Keep extra SOL for network fees. New tokens may require a one-time token account fee.

### Make a swap

Main menu: `🟢 Buy` or `🔴 Sell` (or `/buy` / `/sell`).

1. Pick the pair and enter an amount.
2. Set slippage tolerance — tighter reduces bad fills but raises failure risk.
3. Review the route (expected output and price impact), then confirm.

FatCat routes across liquidity sources with MEV-protected routing and settles output tokens to your wallet.

### Troubleshooting

* **Failed on slippage** — increase tolerance, reduce size in thin liquidity, avoid fast markets.
* **Insufficient SOL** — keep extra for fees and one-time token account creation.
* **Output lower than expected** — check price impact and trade smaller chunks in low liquidity.

### Related

[Market Buy & Market Sell](market-buy-and-market-sell.md) · [Limit Orders](../limit-orders.md) · [Trade Safely](../../safety-and-security/trade-safely.md)
