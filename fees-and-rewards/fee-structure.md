# Fee Structure

FatCat charges product fees on trades and positions.

Some actions run on **Jupiter programs**, which add Jupiter program fees.

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

**Perps**

* **Open:** FatCat **0.08%** + Jupiter **0.06%** (+ borrow fees while open) (+ Solana network fees)
* **Close:** FatCat **No Fee** + Jupiter **0.06%** (+ Solana network fees)
* **Set SL or TP:** FatCat **No Fee** (+ Solana network fees)
  {% endhint %}

Jump to:

* [Fee types](#fee-types-what-youre-paying-for)
* [Fee summary](#fee-summary-fatcat-vs-jupiter)
* [What changes your final cost](#what-can-change-your-final-cost)
* [Refunds and cancellations](#refunds-cancellations-and-why-did-i-pay-a-fee)

### Fee types (what you’re paying for)

* **FatCat fees:** product fees charged by FatCat.
* **Jupiter fees:** program fees charged by Jupiter for specific features (limit, DCA, Perps).
* **Solana network fees:** paid to the network for transactions. These can’t be avoided.

### Where you’ll see fees

You’ll typically see fees in two places:

* **An estimation in the bot summary:** the preview before you confirm.
* **In the approval prompt:** the final review screen (and sometimes multiple transactions).

### Fee summary (FatCat vs Jupiter)

{% tabs %}
{% tab title="Spot (swaps, limit, DCA)" %}

| Action      | FatCat fee | Jupiter fee            | When you’re charged                               |
| ----------- | ---------- | ---------------------- | ------------------------------------------------- |
| Market swap | **0.1%**   | —                      | FatCat: **upfront**                               |
| Limit order | **0.1%**   | **0.1%**               | FatCat: **upfront** / Jupiter: **at fill**        |
| DCA order   | **0.1%**   | **0.1% per execution** | FatCat: **upfront** / Jupiter: **each execution** |

{% tab title="Perps" %}

| Action         | FatCat fee | Jupiter fee             | When you’re charged                             |
| -------------- | ---------- | ----------------------- | ----------------------------------------------- |
| Open position  | **0.08%**  | **0.06% + borrow fees** | FatCat: **at approval** / Jupiter: **deducted** |
| Close position | **No Fee** | **0.06%**               | Jupiter: **deducted**                           |
| Set SL / TP    | **No Fee** | —                       | —                                               |

{% hint style="info" %}
Fees are based on **notional size** (your total position size).

Jupiter borrow fees accrue while the position is open. {% endhint %}

{% hint style="info" %}
Perps can also include a variable **price impact fee** (Jupiter) at execution.
{% endhint %}

See: [Perps](https://docs.fatcatbot.io/trading/perps)
{% endtab %}
{% endtabs %}

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
* **Jupiter program fee** (if the feature runs on Jupiter).
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

<summary>Perps</summary>

* Perps fees are based on **notional size**.
* FatCat charges **0.08%** only when you **open** a position. It’s shown **at approval** and is **non-refundable** once approved.
* Jupiter's **0.06%** fee is charged at **open** and at **close**.
* Borrow fees accrue while the position is open.

</details>

### Related

* Spot execution: [Swaps](https://docs.fatcatbot.io/trading/swaps)
* Target price orders: [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders)
* Scheduled orders: [DCA Orders](https://docs.fatcatbot.io/trading/dca-orders)
* Leverage: [Perps](https://docs.fatcatbot.io/trading/perps)
* Offset fees: [Referrals](https://docs.fatcatbot.io/fees-and-rewards/referrals)
