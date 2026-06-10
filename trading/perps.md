# Perps

Perpetual Futures (Perps) let you open **long** or **short** positions with leverage.

FatCat routes Perps through multiple on-chain venues — **GMTrade** (default), **Jupiter Perpetuals**, and **Flash Trade**. The AI uses GMTrade by default if a token is available across multiple venues; say "Jupiter" or "Flash" when placing a trade via AI to use those instead.

{% hint style="danger" %}
Leverage can liquidate you fast. Size positions conservatively.
{% endhint %}

### What you can do

* Open a long or short with leverage.
* Add to, or partially/fully close, a position.
* Set and manage stop loss (SL) and take profit (TP).

### What you set

* **Market** — Varies by venue; including forex, stocks, commodities, and crypto.
* **Direction** — long or short.
* **Collateral** — the amount you deposit to back the position.
* **Leverage** — your exposure multiplier (maximums vary by venue and market).
* **Slippage tolerance** — default **2%**, adjustable per trade.
* **Optional SL/TP** — trigger-based exits (execution can slip in fast markets).

### Key terms

* **Notional size** — total position size (collateral × leverage).
* **Liquidation price** — the price at which your loss equals your collateral; the position is force-closed and you lose it.
* **Borrow/funding fees** — ongoing costs charged by the venue while a position is open.

### Fees

Perps have a **FatCat fee** plus **venue fees** and **Solana network fees**.

* **FatCat:** **0.06%** of notional, charged only when you **open** (non-refundable, paid in SOL). No FatCat fee to close or to set/modify SL/TP.
* **Venue (GMTrade / Jupiter / Flash Trade):** each charges its own open, close, and ongoing borrow/funding fees. These are set by the venue, can change, and are shown in the in-app approval before you sign.

Full overview: [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

### Opening a position in the bot

1. Tap `📈 Open Long` or `📉 Open Short`.
2. Set token, collateral, leverage, and slippage.
3. Review the summary — liquidation price, position size, collateral, leverage.
4. Tap `✅ Confirm Trade`, then approve.

{% hint style="info" %}
Collateral requirements vary by venue and direction and are shown when you trade. If you pay in a different token, a swap is bundled into the same transaction. Opening another position of the same market and direction updates the existing one.
{% endhint %}

### After you confirm

Positions live in the venue's on-chain program; PnL updates with price moves and ongoing fees, and liquidation can force-close the position if margin gets too low.

{% hint style="warning" %}
SL/TP and liquidation are on-chain rules, not guaranteed fills — fast markets can slip, and liquidation can close you before your SL. After adding to or partially closing a position, re-check liquidation price, SL/TP, and leverage in `🎯 Active Positions`.
{% endhint %}

### Manage & troubleshoot

Manage open positions in `🎯 Active Positions` — see [Manage positions](https://docs.fatcatbot.io/trading/perps/manage-positions). Closed positions are in `📚 Perp History`.

If an action fails, it's usually: not enough SOL for fees, the wrong collateral type, slippage too tight, or a position too large for the venue's pool (try a smaller size or another venue).
