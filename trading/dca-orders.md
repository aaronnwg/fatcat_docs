# DCA Orders

Dollar Cost Averaging (DCA) automates recurring buys or sells over time, splitting your order into smaller trades at regular intervals to reduce the impact of short-term volatility.

#### How it works

You choose a token, total amount, number of orders, and interval. FatCat splits the total into equal portions and executes each at market price through Jupiter's on-chain DCA program. Funds sit in a Jupiter program vault — FatCat has no custody and no access to your key.

### What you set

* **Total amount** — the full size across all executions.
* **Frequency** — minutes (min 5), hours, days, or weeks.
* **Split** — how many executions, and the size of each.

### Requirements and fees

* **Minimum total:** **$100**. **Minimum per execution:** **$50**. Each split must be equal-sized with no leftover.
* **FatCat fee:** **0.1%** upfront. **Jupiter program fee:** per execution. Plus Solana network fees. See [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

{% hint style="info" %}
The first execution runs immediately when you confirm. The schedule is on-chain, so you don't need to keep the bot open.
{% endhint %}

### Create a DCA order

Main menu: `⏰ DCA` → `🟢 DCA Buy` or `🔴 DCA Sell`. Set the token, total amount, and frequency, then confirm and approve. Funds are committed upfront, remaining executions run automatically, and assets land in your wallet after each one.

Manage orders: [Active DCA Orders](https://docs.fatcatbot.io/trading/dca-orders/active-dca-orders) · [DCA Order History](https://docs.fatcatbot.io/trading/dca-orders/dca-order-history).

{% hint style="warning" %}
DCA reduces timing risk, but not market risk. Prices can move between executions.
{% endhint %}
