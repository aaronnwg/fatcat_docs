---
description: Trade Perps across Jupiter and GMTrade with leverage and risk controls.
icon: infinity
---

# Perps

Perpetual Futures (Perps) allow you to place **long** or **short** orders with leverage.

FatCat supports two on-chain venues:

* Jupiter Perpetuals — SOL, wBTC, wETH.
* GMTrade — broader market coverage: crypto, forex, stocks, and commodities. USDC-collateralized.

{% hint style="danger" %}
Leverage can liquidate you fast. Size positions conservatively.
{% endhint %}

### What you can do

* Open a long or short with leverage (max leverage varies by market).
* Add to an existing position (same market + direction).
* Close a position (partial or full).
* Set and manage stop loss (SL) and take profit (TP).

### What you set

* **Market:** any Jupiter or GMTrade market.
* **Direction:** long or short.
* **Collateral amount:** the amount you deposit to back the position.
* **Leverage:** set your exposure multiplier.
* **Slippage tolerance:** default **2%** (adjustable per trade).
* **Optional Stop Loss/Take Profit (SL/TP):** trigger-based exits (execution can slip in fast markets).

### Perps Commands:

Main menu: `💸 PERPS`

* `/open_long`
* `/open_short`
* `/active_positions`
* `/historical_positions`

### Buttons

Trade Perps in the bot from the **Main Menu**.

* `📈 Open Long` — open a long position using FatCat Bot on Telegram.
* `📉 Open Short` — open a short position using FatCat Bot on Telegram.
* `🎯 Active Positions` — view/manage open positions. See: [Manage positions](manage-positions.md).
* `📚 History` — view closed positions and events. See: [Perp History](perp-history.md).

### Supported markets

Jupiter Perpetuals: SOL, wBTC, wETH.

GMTrade: 39 crypto pairs, 7 forex pairs, 10 stock pairs, and 6 commodities.<br>

### Requirements and limits

#### Jupiter Perpetuals

| Setting            | Value                         |
| ------------------ | ----------------------------- |
| Minimum collateral | **$10** equivalent            |
| Leverage           | **1.1× to 250×**              |
| Default slippage   | **2%** (adjustable per trade) |

#### GMTrade

| Setting            | Value                                                                           |
| ------------------ | ------------------------------------------------------------------------------- |
| Minimum position   | Per-market (read live from the market)                                          |
| Minimum collateral | Per-market, typically **$1** (read live from the market)                        |
| Leverage           | **1.1×** to per-market max (range typically **50× – 500×** depending on market) |
| Default slippage   | <p><strong>2%</strong> (adjustable per trade)<br></p>                           |

{% hint style="info" %}
Key terms:

* **Notional size:** your total position size (collateral × leverage).
* **Collateral:** the funds you deposit to back the position.
* **Leverage:** multiplier on collateral (example: 10× = 10× exposure).
* **Liquidation price:** the price at which your loss on notional equals your deposited collateral. The position is force-closed and you lose all your collateral.
* **Borrow fee:** variable cost paid while the position is open.
{% endhint %}

### Perps fees (FatCat + venue)

Perps have **FatCat fees** and **venue program fees**.

Fees are charged as a percentage of **notional size** (your total position size).

You also pay **Solana network fees** for on-chain transactions.

Full fee overview: [Fee Structure](../../fees-and-rewards/fee-structure.md)

#### FatCat fees

| Action                  | Fee                        | When charged                     |
| ----------------------- | -------------------------- | -------------------------------- |
| Open position           | **0.08%** of notional size | At approval (**non-refundable**) |
| Close position (market) | No fee                     | —                                |
| Set stop loss           | No fee                     | —                                |
| Set take profit         | No fee                     | —                                |
| Modify SL/TP            | No fee                     | —                                |
| Cancel SL/TP            | No fee                     | —                                |

{% hint style="info" %}
FatCat only charges a fee when you **open** a position. The FatCat fee is paid in **SOL**.
{% endhint %}

#### Jupiter fees

| Fee type         | Amount                     | When applied                    |
| ---------------- | -------------------------- | ------------------------------- |
| Open position    | **0.06%** of notional      | Deducted from position at open  |
| Close position   | **0.06%** of notional      | Deducted from position at close |
| Borrow fee       | Variable (hourly)          | Ongoing while position is open  |
| Price impact fee | Variable (depends on size) | Deducted at execution           |

{% hint style="info" %}
Jupiter uses a **borrow fee** system (not funding rates).

Borrow fees accrue hourly, depend on pool utilization, and are paid to liquidity providers.
{% endhint %}

#### GMTrade fees

| Fee type        | Amount                                                                                                        | When applied                        |
| --------------- | ------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| Open position   | Up to **0.04%** (positive impact) or **0.06%** (negative impact) of position size; actual rate set per market | Deducted from position at execution |
| Close position  | Up to **0.04%** (positive impact) or **0.06%** (negative impact) of position size; actual rate set per market | Deducted from position at execution |
| Borrow fee      | Variable (per-second, separate rates for long and short)                                                      | Accrues while the position is open  |
| Funding fee     | Variable (flows between longs and shorts)                                                                     | Accrues while the position is open  |
| Price impact    | Variable (depends on size vs. pool depth)                                                                     | Deducted at execution               |
| Liquidation fee | Charged at liquidation                                                                                        | Deducted from remaining collateral  |

{% hint style="info" %}
Per GMTrade's published fee schedule, the open and close fee is up to **0.04%** when your trade improves the balance of longs and shorts on that market, and up to **0.06%** when it worsens the balance.

Each market sets its own rates on-chain. The live percentage and dollar amount are shown in the in-app approval before you sign and may be lower than these ceilings.
{% endhint %}

{% hint style="info" %}
GMTrade uses both borrow fees and funding fees:

* **Borrow fee:** accrues per second, with separate rates for longs and shorts that scale with pool utilization. The borrow long and borrow short rates are shown in the GMTrade trade preview.
* **Funding fee:** flows between longs and shorts in proportion to open-interest imbalance. The side with more open interest pays the other.
{% endhint %}

<details>

<summary>Advanced: account rent</summary>

A small SOL rent amount can be required to create an escrow account. It is returned when you close the position.

</details>

### Opening a position (long or short) with the Telegram bot

The buttons and the `/open_long` / `/open_short` commands trade Jupiter markets only (SOL, wBTC, wETH).

To trade GMTrade markets from the Telegram bot, use the AI chat. The AI can open positions on either venue, and defaults to GMTrade — say "Jupiter" / "Jup" when asking the AI if you want Jupiter instead.

The web app supports both venues, selectable per trade.

{% stepper %}
{% step %}
### Choose long or short

Tap `📈 Open Long` or `📉 Open Short`.
{% endstep %}

{% step %}
### Configure the position

Use the buttons to set:

| Setting    | Button                  | Description                             |
| ---------- | ----------------------- | --------------------------------------- |
| Token      | `🌟 Select Token`       | SOL, wBTC, or wETH                      |
| Collateral | `💳 Collateral Amount`  | Amount to use as collateral             |
| Leverage   | `💠 Choose Leverage`    | 1.1× to 250×                            |
| Slippage   | `⚙️ Slippage Tolerance` | Custom slippage tolerance (default: 2%) |
{% endstep %}

{% step %}
### Review the summary

Before you confirm, review:

* Estimated liquidation price
* Total position size
* Collateral amount
* Leverage
{% endstep %}

{% step %}
### Confirm and approve

Tap `✅ Confirm Trade`, then review and approve.
{% endstep %}
{% endstepper %}

#### Collateral requirements

**Opening a position with the Telegram bot**

| Position type | Required collateral                           |
| ------------- | --------------------------------------------- |
| Long          | The token you're longing (SOL, wBTC, or wETH) |
| Short         | USDC                                          |

**Opening a position with the web app or AI assistant**

| Position type | Required collateral            |
| ------------- | ------------------------------ |
| Long or Short | USDC, wBTC, wETH, USDT, or SOL |

{% hint style="info" %}
If you pay in something other than the position's underlying asset, a Jupiter swap is added to the same atomic transaction.

You sign once, and the swap and the position both land — or neither does.
{% endhint %}

#### Adding to an existing position

If you already have an open position of the same market(example: Jupiter venue, SOL long) and open another, the existing position is updated instead of a separate one being created.

You’ll see a modified summary showing:

* Modified position size
* Modified liquidation price
* Modified total collateral
* New effective leverage

### What happens after you confirm

* **Position account:** stores collateral, leverage, and settings.
* **Pricing:** uses oracles and on-chain logic for triggers.
* **PnL:** updates with price movements and ongoing fees.
* **Liquidation:** can force-close if margin gets too low.

<details>

<summary>SL/TP + liquidation: trigger vs execution (important)</summary>

SL/TP and liquidation are **on-chain rules**, but they’re not “perfect fills”.

Keep these mental models:

* **Trigger vs execution:** your SL/TP trigger can be reached, then execution happens at the best available on-chain price.
* **Fast markets can slip:** you can exit worse than your trigger in big moves.
* **Liquidation can win the race:** if margin gets too low, liquidation can close you before your SL.
* **After size changes:** if you add to a position or close partially, re-check:
  * liquidation price
  * your SL/TP levels
  * your effective leverage

Always confirm current status in `🎯 Active Positions`.

</details>

### Managing active positions

Open `🎯 Active Positions`, then tap a position to manage it.

Full guide: [Manage positions](manage-positions.md).

### Troubleshooting

If an action fails or looks “off”, it’s usually one of these:

* **Not enough SOL:** you need SOL for network fees (and sometimes account rent).
* **Slippage too tight:** increase slippage tolerance for fast markets.
* **PnL drifting while price is flat:** borrow or funding fees can accrue while the position is open.
* **Liquidation price changed:** effective leverage changes after you add collateral/size, or as fees accrue.

If you’re still stuck, try again with smaller size and higher slippage.
