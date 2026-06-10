---
description: Trade Perps with leverage and risk controls.
icon: infinity
---

# Perps

Perpetual Futures (Perps) let you open **long** or **short** positions with leverage.

FatCat routes Perps through multiple on-chain venues — **GMTrade**, **Jupiter Perpetuals**, and **Flash Trade** — covering SOL, BTC, ETH, and many other markets (some venues also cover forex, stocks, and commodities).

{% hint style="danger" %}
Leverage can liquidate you fast. Size positions conservatively.
{% endhint %}

### What you can do

* Open a long or short with leverage (maximums vary by venue and market).
* Add to, or partially/fully close, a position.
* Set and manage stop loss (SL) and take profit (TP).

### What you set

* **Market** — varies by venue.
* **Direction** — long or short.
* **Collateral** — the amount you deposit to back the position.
* **Leverage** — your exposure multiplier.
* **Slippage tolerance** — default **2%**, adjustable per trade.
* **Optional SL/TP** — trigger-based exits (execution can slip in fast markets).

### Key terms

* **Notional size** — total position size (collateral × leverage).
* **Liquidation price** — the price at which your loss equals your collateral; the position is force-closed and you lose it.
* **Borrow/funding fees** — ongoing costs charged by the venue while a position is open.

### Fees

Perps have a **FatCat fee** plus **venue fees** and **Solana network fees**, all charged on notional size.

* **FatCat:** **06%** of notional, charged only when you **open** (non-refundable, paid in SOL). No FatCat fee to close or to set/modify SL/TP.
* **Venue (GMTrade / Jupiter / Flash Trade):** each charges its own open, close, and ongoing borrow/funding fees. These are set by the venue, can change, and are shown in the in-app approval before you sign.

Full overview: [Fee Structure](../../fees-and-rewards/fee-structure.md).

### Opening a position

In the Telegram bot, the `📈 Open Long` / `📉 Open Short` buttons trade a default venue's markets. To reach other venues and markets, use the **AI chat** or the **web app**, which support all venues — name the venue (e.g. "Jupiter" or "Flash") when you want a specific one.

1. Tap `📈 Open Long` or `📉 Open Short` (or ask the AI / use the web app).
2. Set token, collateral, leverage, and slippage.
3. Review the summary — liquidation price, position size, collateral, leverage.
4. Tap `✅ Confirm Trade`, then approve.

{% hint style="info" %}
Collateral requirements vary by venue and direction, and are shown when you trade. If you pay in a different token, a swap is bundled into the same transaction — you sign once and both land, or neither does. Opening another position of the same market and direction updates the existing one.
{% endhint %}

### After you confirm

Positions live in the venue's on-chain program; PnL updates with price moves and ongoing fees, and liquidation can force-close the position if margin gets too low.

{% hint style="warning" %}
SL/TP and liquidation are on-chain rules, not guaranteed fills — fast markets can slip, and liquidation can close you before your SL. After adding to or partially closing a position, re-check liquidation price, SL/TP, and leverage in `🎯 Active Positions`.
{% endhint %}

### Manage & troubleshoot

Manage open positions in `🎯 Active Positions` — see [Manage positions](manage-positions.md). Closed positions are in [Perp History](perp-history.md).

If an action fails, it's usually: not enough SOL for fees, slippage too tight, the wrong collateral type, or a position too large for the venue's pool (try a smaller size or another venue).
