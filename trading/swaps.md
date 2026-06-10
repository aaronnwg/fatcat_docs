# Swaps

Swaps are **market orders** — they execute instantly at the best available route. For price-triggered trades, see [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders).

### Before you swap

* You need a wallet ([Setting Up Your Wallet](https://docs.fatcatbot.io/overview/getting-started/setting-up-your-wallet)).
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

[Market Buy & Market Sell](https://docs.fatcatbot.io/trading/swaps/market-buy-and-market-sell) · [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders) · [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely)
