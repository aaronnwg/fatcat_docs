# Perps

Perpetual Futures (Perps) allow you to place **long** or **short** orders with leverage.

Execution runs on **Jupiter’s on-chain Perpetuals program**.

The markets we currently support are **SOL**, **wBTC**, and **wETH** Perps.

{% hint style="danger" %}
Leverage can liquidate you fast. Size positions conservatively.
{% endhint %}

### What you can do

* Open a long or short with up to **250×** leverage.
* Add to an existing position (same market + direction).
* Close a position (partial or full).
* Set and manage stop loss (SL) and take profit (TP).

### What you set

* **Market:** SOL, wBTC, or wETH.
* **Direction:** long or short.
* **Collateral amount:** set your position size (the amount you lock).
* **Leverage:** set your exposure multiplier.
* **Slippage tolerance:** default **2%** (adjustable per trade).
* **Optional Stop Loss/Take Profit (SL/TP):** trigger-based exits (execution can slip in fast markets).

### Perps Commands:

Main menu: `💸 PERPS`

* `/open_long`
* `/open_short`
* `/active_positions`
* `/historical_positions`
* `/perps_mobile_app`

### Buttons

Trade Perps in the bot, or open the **Perps Mobile App** directly from the bot’s **Main Menu** for a chart-first experience.

* `📱 Perps Mobile App` (Main Menu) — charts + faster mobile management. See: [Perps Mobile App](https://docs.fatcatbot.io/trading/broken-reference).
* `📈 Open Long` — open a long position using FatCat Bot on Telegram.
* `📉 Open Short` — open a short position using FatCat Bot on Telegram.
* `🎯 Active Positions` — view/manage open positions. See: [Manage positions](https://docs.fatcatbot.io/trading/perps/manage-positions).
* `📚 History` — view closed positions and events. See: [Position History](https://docs.fatcatbot.io/trading/perps/perp-history).

### Supported markets

* **SOL**
* **wBTC**
* **wETH**

### Requirements and limits

| Setting            | Value                         |
| ------------------ | ----------------------------- |
| Minimum collateral | **$10** equivalent            |
| Leverage           | **1.1× to 250×**              |
| Default slippage   | **2%** (adjustable per trade) |

{% hint style="info" %}
Key terms:

* **Notional size:** your total position size. It includes leverage.
* **Collateral:** what you lock to support the position.
* **Leverage:** multiplier on collateral (example: 10× = 10× exposure).
* **Liquidation price:** price where margin becomes too low. The position can be force-closed.
* **Borrow fee:** hourly cost paid while the position is open.
  {% endhint %}

### Perps fees (FatCat + Jupiter)

Perps have **FatCat fees** and **Jupiter program fees**.

Most fees are charged as a percentage of **notional size** (your total position size).

You also pay **Solana network fees** for on-chain transactions.

Full fee overview: [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure)

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
FatCat only charges a fee when you **open** a position.
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

{% hint style="info" %}
Rule of thumb for open + close fees: **0.20% total** (FatCat **0.08%** on open + Jupiter **0.12%**).

Then add borrow fees if you hold the position.
{% endhint %}

<details>

<summary>Advanced: rent + Jupiter reference</summary>

A small SOL rent amount can be required to create an escrow account. It is returned when you close the position.

</details>

### Opening a position (long or short)

{% stepper %}
{% step %}

### Choose long or short

Tap `📈 Open Long` or `📉 Open Short`.
{% endstep %}

{% step %}

### Configure the position

Use the buttons to set:

| Setting       | Button                  | Description                             |
| ------------- | ----------------------- | --------------------------------------- |
| Token         | `🌟 Select Token`       | SOL, wBTC, or wETH                      |
| Collateral    | `💳 Collateral Amount`  | Amount to use as collateral             |
| Leverage      | `💠 Choose Leverage`    | 1.1× to 250×                            |
| Slippage      | `⚙️ Slippage Tolerance` | Custom slippage tolerance (default: 2%) |
| {% endstep %} |                         |                                         |

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

| Position type | Required collateral                                    |
| ------------- | ------------------------------------------------------ |
| Long          | Must use the token you’re longing (SOL, wBTC, or wETH) |
| Short         | Must use USDC                                          |

#### Adding to an existing position

If you already have an open position of the same type (example: SOL long) and open another, FatCat updates the existing position instead of creating a separate one.

You’ll see a modified summary showing:

* Modified position size
* Modified liquidation price
* Modified total collateral
* New effective leverage

### What happens after you confirm

* **Position account:** stores collateral, leverage, and settings.
* **Pricing:** uses oracles and on-chain logic for triggers.
* **PnL:** updates with price movements and borrow costs.
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

<details>

<summary>On-chain behavior (details)</summary>

* Positions live in Jupiter’s Perpetuals Program accounts.
* SL and TP are enforced by on-chain rules.
* Liquidations protect the underlying liquidity pool.

</details>

### Managing active positions

Open `🎯 Active Positions`, then tap a position to manage it.

Full guide: [Manage positions](https://docs.fatcatbot.io/trading/perps/manage-positions).

You can also manage Perps directly on Jupiter (optional): <https://jup.ag/perps>

### Troubleshooting

If an action fails or looks “off”, it’s usually one of these:

* **Not enough SOL:** you need SOL for network fees (and sometimes account rent).
* **Wrong collateral type:** longs require the market token. Shorts require **USDC**.
* **Slippage too tight:** increase slippage tolerance for fast markets.
* **PnL drifting while price is flat:** borrow fees accrue hourly while the position is open.
* **Liquidation price changed:** effective leverage changes after you add collateral/size, or as fees accrue.

If you’re still stuck, try again with smaller size and higher slippage.
