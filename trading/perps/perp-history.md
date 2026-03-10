# Perp History

**Button:** `📚 Perp History` (Perps menu)\
Command: `/historical_positions`

### What you’ll see

Perp History shows **events** in reverse-chronological order (newest first).

Common event types:

* **Open Long Position**.
* **Open Short Position.**
* **Trigger Close Position (SL/TP).**
* **Close Position.**
* **Liquidation.**

### Closed-position PnL

You’ll see realized PnL when a position is closed.

Fully closed positions show a final PnL summary.

Click an event PnL card to view a closed position’s PnL.

### PnL cards

When you close a position, FatCat generates a shareable PnL card.

PnL cards are useful for sharing trade results.

{% hint style="warning" %}
The PnL shown in History and on PnL cards includes close fees and borrow fees deducted by Jupiter’s Perp program.

It does **not** include FatCat fees charged at approval.

It also does not include Jupiter's opening fees.

Full breakdown: [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).
{% endhint %}

<details>

<summary>If my latest event isn’t showing</summary>

Reopen `📚 Perp History` after a short delay.

On-chain finality and indexing can take a moment during congestion.

</details>
