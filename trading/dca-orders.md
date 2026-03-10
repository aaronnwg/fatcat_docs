# DCA Orders

Dollar Cost Averaging (DCA) lets you automate recurring buys or sells of a token over time.

Instead of buying all at once, DCA splits your order into smaller trades executed at regular intervals.

#### Why use DCA?

* Reduces the impact of short-term price volatility.
* Automates your trading strategy.
* Useful for accumulating a position over time or gradually selling.

#### How DCA works

1. You choose a token, a total amount, a number of orders, and a time interval.
2. FatCat splits your total amount into equal portions.
3. At each interval, a swap is automatically executed at the current market price through Jupiter’s on-chain DCA program.
4. This continues until all orders are filled or you cancel.

Your funds are deposited into a Program Derived Address (PDA) controlled by Jupiter’s smart contract.

Jupiter’s keeper network executes the swaps on schedule.

FatCat has no custody of your funds during this process and no access to your private key.

### Before you start

* Verify the token mint address from a trusted source.
* Keep extra SOL for network fees.
* Expect price moves between executions.

See also: [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely) and [Where to Find Tokens](https://docs.fatcatbot.io/tokens/where-to-find-tokens).

### What you can do

* **Buy:** swap **SOL → token** on a schedule.
* **Sell:** swap **token → SOL** on a schedule.

### What you set

* **Total amount:** the full size across all executions.
* **Frequency:** minutes, hours, days, or weeks between executions.
* **Split:** how many executions (and the size of each execution).

### Where to find it

Main menu: `⏰ DCA`

### DCA menu options

* `🟢 DCA Buy` — set up recurring buy orders
* `🔴 DCA Sell` — set up recurring sell orders
* `🗓️ Active DCA Orders` — view and manage active DCA orders
* `📔 DCA Order History` — view completed DCA orders

### Requirements and limits

* **Minimum total size:** **$100** equivalent.
* **Minimum per execution:** **$50** equivalent.
* **Frequency:** Minutes (**min 5**), Hours, Days, or Weeks.

#### Fees

* **FatCat fee:** **1%** (charged upfront)
* **Jupiter fee:** **0.1%** (deducted per swap)

For the full fee breakdown, see [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

{% hint style="info" %}
The first execution is placed **immediately** when you confirm and approve.

You do not need to keep the bot open. The schedule is on-chain.
{% endhint %}

### How sizing works

After you enter a total amount and a frequency, FatCat proposes valid splits.

Each split must satisfy:

* Each execution is **≥ $50** equivalent.
* The total divides cleanly into equal-sized executions. No “leftover” amount remains.

You pick the split you want and confirm.

### Create a DCA order

When you confirm a DCA, you’ll see an in-app approval screen.

Review the summary, then approve.

There is no separate wallet app.

{% tabs %}
{% tab title="DCA Buy" %}

#### DCA Buy setup

1. Tap `⏰ DCA` → `🟢 DCA Buy`.
2. Configure the order:
   * `🌟 Token to Buy` — Paste the token mint address.
   * `💠 Set Total DCA Amount`
   * `🔁 Set DCA Frequency`
3. Tap `✅ Confirm DCA Setup`.
4. Review and approve. Your funds are commited upfront.
   {% endtab %}

{% tab title="DCA Sell" %}

#### DCA Sell setup

1. Tap `⏰ DCA` → `🔴 DCA Sell`.
2. Configure the order:
   * `🌟 Token to Sell`
   * `💠 Set Total DCA Amount`
   * `🔁 Set DCA Frequency`
3. Tap `✅ Confirm DCA Setup`.
4. Review and approve.
   {% endtab %}
   {% endtabs %}

### What happens after you confirm

* **Funds custody:** funds are held in a **program-owned vault** linked to your wallet.
* **Scheduling:** remaining executions are queued on-chain until done or cancelled.
* **Execution:** keeper services trigger each execution at the scheduled time.
* **Settlement:** after each execution, assets are sent to **your wallet**.

<details>

<summary>On-chain behavior (details)</summary>

* DCA uses Jupiter’s on-chain recurring program.
* Orders, schedules, and funds live on-chain in a program-owned vault.
* Keepers continuously scan for due executions and submit the transactions.
* The schedule stays active until the order completes or is cancelled.

</details>

### Manage DCA orders

* View and cancel active orders: [Active DCA Orders](https://docs.fatcatbot.io/trading/dca-orders/active-dca-orders)
* Review past orders: [DCA Order History](https://docs.fatcatbot.io/trading/dca-orders/dca-order-history)

### Troubleshooting

If setup fails or you don’t see the split you want, it’s usually one of these:

* The total is below **$100** equivalent at setup time.
* One of the executions would be below **$50** equivalent.
* The total does not divide into equal-sized executions (no leftover allowed).
* Your wallet balance is too low for the total (plus fees).

{% hint style="warning" %}
DCA reduces timing risk, but it does not remove market risk. Prices can move between executions.
{% endhint %}
