---
description: >-
  FatCat, venue, and Solana network fees for swaps, DCA, limit orders, and
  Perps.
icon: arrow-up-right-dots
---

# Fee Structure

FatCat charges product fees on trades and positions.

Actions that run on **Jupiter programs** or the **GMTrade program** add venue program fees.<br>

All on-chain actions also pay **Solana network fees**.

{% hint style="info" %}
Fees shown here are current as of **Feb 10, 2026**.

You’ll always see the exact upfront cost in the in-app approval screen **during approval**.
{% endhint %}

{% hint style="info" %}
You pay fees at approval/execution.
{% endhint %}

{% hint style="info" %}
At a glance

**Spot**

* **Market swaps:** FatCat **0.1%** (+ Solana network fees)
* **Limit orders:** FatCat **0.1%** + Jupiter **0.1%** (+ Solana network fees)
* **DCA orders:** FatCat **0.1%** + Jupiter **0.1% per execution** (+ Solana network fees)

**Perps — GMTrade**

* **Open:** FatCat **0.08%** + GMTrade up to **0.04%–0.06%** (actual rate set per market; shown at approval) (+ borrow & funding fees while open) (+ Solana network fees)
* **Close:** FatCat **No Fee** + GMTrade up to **0.04%–0.06%** (actual rate set per market; shown at approval) (+ Solana network fees)
* **Set SL or TP:** FatCat **No Fee** (+ Solana network fees)

**Perps — Jupiter**

* **Open:** FatCat **0.08%** + Jupiter **0.06%** (+ borrow fees while open) (+ Solana network fees)
* **Close:** FatCat **No Fee** + Jupiter **0.06%** (+ Solana network fees)
* **Set SL or TP:** FatCat **No Fee** (+ Solana network fees)
{% endhint %}

Jump to:

* [Fee types](fee-structure.md#fee-types-what-youre-paying-for)
* [Fee summary](fee-structure.md#fee-summary)
* [What changes your final cost](fee-structure.md#what-can-change-your-final-cost)
* [Refunds and cancellations](fee-structure.md#refunds-cancellations-and-why-did-i-pay-a-fee)

### Fee types (what you’re paying for)

* **FatCat fees:** product fees charged by FatCat.
* **Jupiter fees:** program fees charged by Jupiter for specific features (limit, DCA, Jupiter Perps).
* **GMTrade fees:** program fees charged by GMTrade for GMTrade Perps.<br>
* **Solana network fees:** paid to the network for transactions. These can’t be avoided.

### Where you’ll see fees

You’ll typically see fees in two places:

* **An estimation in the bot summary:** the preview before you confirm.
* **In the approval prompt:** the final review screen (and sometimes multiple transactions).

{% hint style="info" %}
If you’re unsure, treat the bot summary as an estimate.

Treat the approval prompt as the source of truth.
{% endhint %}

### Fee summary

{% tabs %}
{% tab title="Spot (swaps, limit, DCA)" %}
| Action      | FatCat fee | Jupiter fee            | When you’re charged                               |
| ----------- | ---------- | ---------------------- | ------------------------------------------------- |
| Market swap | **0.1%**   | —                      | FatCat: **upfront**                               |
| Limit order | **0.1%**   | **0.1%**               | FatCat: **upfront** / Jupiter: **at fill**        |
| DCA order   | **0.1%**   | **0.1% per execution** | FatCat: **upfront** / Jupiter: **each execution** |

{% hint style="info" %}
Limit and DCA run on Jupiter programs.

That’s why they can include Jupiter fees.
{% endhint %}
{% endtab %}

{% tab title="Perps — GMTrade" %}
| Action         | FatCat fee | GMTrade fee                                                   | When you’re charged                             |
| -------------- | ---------- | ------------------------------------------------------------- | ----------------------------------------------- |
| Open position  | **0.08%**  | Up to **0.04%–0.06%** order fee (per market) + borrow/funding | FatCat: **at approval** / GMTrade: **deducted** |
| Close position | **No Fee** | Up to **0.04%–0.06%** order fee (per market)                  | GMTrade: **deducted**                           |
| Set SL / TP    | **No Fee** | —                                                             | —                                               |
{% endtab %}

{% tab title="Perps — Jupiter" %}
| Action         | FatCat fee | Jupiter fee             | When you’re charged                             |
| -------------- | ---------- | ----------------------- | ----------------------------------------------- |
| Open position  | **0.08%**  | **0.06% + borrow fees** | FatCat: **at approval** / Jupiter: **deducted** |
| Close position | **No Fee** | **0.06%**               | Jupiter: **deducted**                           |
| Set SL / TP    | **No Fee** | —                       | —                                               |
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Perps fees are based on **notional size** (your total position size).
{% endhint %}

See: [Perps](../trading/perps/)

{% hint style="info" %}
Timing glossary:

* **Upfront:** charged before execution.
* **At fill:** charged when the order executes.
* **At approval:** shown when you approve the action.
* **Deducted:** taken from collateral or trade amounts.
{% endhint %}

### What can change your final cost

Fees are predictable. Execution costs can move.

* **Solana network fees:** can rise with congestion (priority fees).
* **Price impact / slippage:** depends on liquidity and size at execution.
* **Perps borrow fees:** accrue while the position stays open.
* **GMTrade funding fees:** accrue while the position stays open.
* **GMTrade order fee:** varies per market; shown at approval.<br>
* **Limit / DCA behavior:** Jupiter fees apply on actual fills/executions (partial fills can mean partial fees).

### Refunds, cancellations, and “why did I pay a fee?”

{% hint style="warning" %}
Some fees are charged **upfront** or **at approval**.

Those fees are usually **non-refundable**, even if you cancel later.
{% endhint %}

<details>

<summary>Why do I see multiple fees on one action?</summary>

It’s normal to see a mix of:

* **FatCat fee** (product fee).
* **Venue program fee**.
* **Solana network fees** (to submit transactions).

These are separate payees and separate fee rules.

</details>

<details>

<summary>Why did I pay a fee if my transaction failed?</summary>

Solana network fees are paid when a transaction is processed.

That can happen even if the transaction fails due to slippage or simulation errors.

</details>

<details>

<summary>Market swaps</summary>

* FatCat fee is charged **upfront**.
* Solana network fees are paid when the transaction is sent.
* If the transaction fails, network fees can still be paid.

</details>

<details>

<summary>Limit orders</summary>

* FatCat fee is charged **upfront** when you place the order.
* Jupiter fee is charged **only if it fills**.
* Cancelling an order stops execution. It does not undo already-paid fees.

</details>

<details>

<summary>DCA orders</summary>

* FatCat fee is charged **upfront** when you set up the DCA.
* Jupiter fee is charged **per execution**.
* Cancelling stops **future** executions only.

</details>

<details>

<summary>Perps — GMTrade</summary>

* Perps fees are based on **notional size**.
* FatCat charges **0.08%** only when you **open** a position. It’s shown **at approval** and is **non-refundable** once approved. Paid in **SOL**.
* GMTrade charges up to **0.04%** or **0.06%** on open and on close. The rate is set per-market on-chain and may be lower than these ceilings. The in-app approval shows the live figure.
* Borrow fees accrue per second while the position is open, with separate rates for longs and shorts.
* Funding fees flow between longs and shorts.
* A variable price impact is deducted at execution.

</details>

<details>

<summary>Perps — Jupiter</summary>

* Perps fees are based on **notional size**.
* FatCat charges **0.08%** only when you **open** a position. It’s shown **at approval** and is **non-refundable** once approved. Paid in **SOL**.
* Jupiter's **0.06%** fee is charged at open and at close.
* Borrow fees accrue while the position is open.

</details>

### Related

* Spot execution: [Swaps](../trading/swaps/)
* Target price orders: [Limit Orders](../trading/limit-orders.md)
* Scheduled orders: [DCA Orders](../trading/dca-orders/)
* Leverage: [Perps](../trading/perps/)
* Offset fees: [Referrals](referrals.md)
