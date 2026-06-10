# Fee Structure

FatCat charges product fees on trades and positions. Some actions run on programs (Jupiter, GMTrade, Flash Trade) that charge their own fees, and all on-chain actions pay **Solana network fees**.

{% hint style="info" %}
You'll always see the exact cost in the in-app approval screen before you confirm.
{% endhint %}

### At a glance

* **Market swaps:** FatCat **0.1%**
* **Limit orders:** FatCat **0.1%** + Jupiter program fee (only if it fills)
* **DCA orders:** FatCat **0.1%** + Jupiter program fee per execution
* **Perps — open:** FatCat **0.08%** of notional (non-refundable, paid in SOL) + venue fees
* **Perps — close / set SL or TP:** FatCat **No Fee** + venue fees

All actions also pay Solana network fees.

### Fee types

* **FatCat fees** — product fees charged by FatCat.
* **Venue fees** — program fees charged by Jupiter, GMTrade, or Flash Trade for the feature you use. These are set by the venue, can change over time, and are shown at approval.
* **Solana network fees** — paid to the network for every transaction; unavoidable.

### Perps fees

* **FatCat:** **0.08%** of notional, only when you **open**. Non-refundable once approved, paid in SOL. No FatCat fee to close or set SL/TP.
* **Venue:** each venue charges its own open, close, and ongoing borrow/funding fees on notional size, shown in the in-app approval.

See [Perps](https://docs.fatcatbot.io/trading/perps).

### What can change your final cost

* Network fees rise with congestion.
* Price impact / slippage depend on liquidity and size.
* Perps borrow/funding fees accrue while a position stays open.
* Limit / DCA venue fees apply on actual fills (partial fills mean partial fees).

{% hint style="warning" %}
Some fees are charged upfront or at approval and are **non-refundable**, even if you cancel later or the transaction fails. Network fees are paid whenever a transaction is processed.
{% endhint %}

### Related

[Swaps](https://docs.fatcatbot.io/trading/swaps) · [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders) · [DCA Orders](https://docs.fatcatbot.io/trading/dca-orders) · [Perps](https://docs.fatcatbot.io/trading/perps) · [Referrals](https://docs.fatcatbot.io/fees-and-rewards/referrals)
