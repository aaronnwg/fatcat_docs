# Swaps

### Swaps (spot trading) vs limit orders

Swaps are **market orders**. They execute instantly.

Limit orders execute only when the price hits your target. See [Limit orders](https://docs.fatcatbot.io/trading/limit-orders).

### Before you swap

* You need a wallet. See [Setting Up Your Wallet](https://docs.fatcatbot.io/overview/getting-started/setting-up-your-wallet).
* Always keep extra **SOL** in your wallet balance for covering network fees.
* New tokens may require a one-time token account creation fee.

### Accessing swaps

* Main menu: `🟢 Buy` or `🔴 Sell`
* Commands: `/buy` or `/sell`

{% hint style="info" %}
Token → token swaps use the same flow. Change both input and output tokens.
{% endhint %}

### What you can do

* **Buy:** swap **SOL → token**.
* **Sell:** swap **token → SOL**.

### Inputs you control

* **Token:** what token you want to buy or sell.
* **Amount:** what you spend or receive.
* **Slippage tolerance:** how much price movement you accept.

{% hint style="info" %}
Tighter slippage reduces bad fills. It increases failure risk.
{% endhint %}

### How execution works

When you confirm, FatCat builds and submits a transaction that:

* Finds the best route across liquidity sources.
* Splits across venues when needed.
* Uses routing with MEV protection to reduce sandwich risk.
* Settles output tokens back to **your wallet**.

### Make a swap

{% stepper %}
{% step %}

### Pick a pair

Choose what you sell and what you buy.
{% endstep %}

{% step %}

### Enter an amount

Set the amount you spend or the amount you want.
{% endstep %}

{% step %}

### Set slippage tolerance

Use tighter slippage in stable markets.
{% endstep %}

{% step %}

### Review the route

Check expected output and price impact.
{% endstep %}

{% step %}

### Confirm

The trade executes on-chain right away.
{% endstep %}
{% endstepper %}

### What happens after you confirm

* **Submission:** the swap is sent to Solana.
* **Execution:** routing chooses the best available path.
* **Settlement:** output assets land in your wallet.
* **Failure cases:** the swap can fail on slippage, liquidity, or fees.

### Troubleshooting

<details>

<summary>Swap failed (slippage)</summary>

* Increase slippage tolerance a bit.
* Reduce size in thin liquidity.
* Avoid fast candles and big news moves.

</details>

<details>

<summary>Swap failed (insufficient SOL)</summary>

* Keep extra SOL for fees.
* You may also need SOL to create a token account once.

</details>

<details>

<summary>Output is lower than expected</summary>

* Check price impact before confirming.
* Tighten slippage when markets are calm.
* Prefer smaller chunks in low liquidity.

</details>

### Related

* [Market Buy & Market Sell](https://docs.fatcatbot.io/trading/swaps/market-buy-and-market-sell)
* [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders)
* [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely)
