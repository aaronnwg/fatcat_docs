---
icon: comments-question
---

# FAQ

Common questions for trading with FatCat Bot in Telegram.

### Start here (quick links)

{% columns %}
{% column %}
**Quick Start Guide**\
Fastest path to your first trade.

Go to: [Quick Start Guide](quick-start-guide.md)

**Setting up your wallet**\
Create your embedded wallet and learn how approvals work.

Go to: [Setting Up Your Wallet](getting-started/setting-up-your-wallet.md)
{% endcolumn %}

{% column %}
**Swaps (spot trading)**\
Market buy/sell basics, slippage, and failed swaps.

Go to: [Swaps](../trading/swaps/)

**Fees**\
What you pay, and when you pay it.

Go to: [Fee Structure](../fees-and-rewards/fee-structure.md)
{% endcolumn %}
{% endcolumns %}

**AI Assistant**\
Research tokens, prepare trades, and manage positions in plain language.

Go to: [AI Assistant](../ai-assistant/ai-assistant.md)

### Jump to a section

* [General](faq.md#general)
* [Wallet and Security](faq.md#wallet-and-security)
* [Trading](faq.md#trading)
* [Limit orders and DCA](faq.md#limit-orders-and-dca)
* [Perps (leveraged trading)](faq.md#perps-leveraged-trading)
* [Fees](faq.md#fees)
* [Telegram and support](faq.md#telegram-and-support)
* [Troubleshooting](faq.md#troubleshooting)
* [Withdraw](faq.md#withdraw)

Need help inside Telegram? Use `🔔 Help` in the bot.

Also see: [Help](../help-and-policies/help.md).

{% hint style="warning" %}
Never share your seed phrase or private key.\
Assume unsolicited support DMs are scams.
{% endhint %}

### Search FAQs

Use the docs **search bar** (top of the site).

For quick in-page search, use:

* macOS: `⌘ + F`
* Windows/Linux: `Ctrl + F`

{% hint style="info" %}
Click or tap a question to expand the answer.
{% endhint %}

### General

<details>

<summary>What is FatCat Bot?</summary>

FatCat Bot is a non-custodial Solana trading bot that runs inside Telegram.

You can swap any Solana token for any other, place limit orders, automate trades with DCA, and trade Perpetual Futures.

</details>

<details>

<summary>Is FatCat Bot free to use?</summary>

FatCat Bot is not free.

Fees are charged on trades. Market swaps are typically around **0.1%**. Opening a Perps position is typically around **0.08%**. You also pay standard Solana network fees and venue program fees where applicable.

See [Fee Structure](../fees-and-rewards/fee-structure.md) for a full breakdown.

</details>

<details>

<summary>Do I need a separate wallet app?</summary>

No.

FatCat supports Privy embedded wallets and wallet connection.

You can create a wallet when you sign in with your email or phone, or connect an existing wallet.

There is nothing to download or install.

</details>

<details>

<summary>Can I use my existing Solana wallet (Solflare, Backpack, etc.)?</summary>

Yes.

You can connect an existing wallet when you sign in.

You can also create a Privy embedded wallet instead, transfer funds into your FatCat wallet address, or export your FatCat wallet’s private key and import it into another wallet at any time.

</details>

<details>

<summary>What is the FatCat Web App?</summary>

The FatCat Web App is a web-based trading interface you can open directly from the bot menu.

Open it from the bot’s **Main Menu**. Tap `📱 FatCat Web App`.

It offers live charts, swaps, limit orders, Perps trading, and portfolio management in a visual interface. It is the recommended way to trade for the best experience.

</details>

<details>

<summary>What is the AI Assistant?</summary>

The AI Assistant is a conversational trading companion built into FatCat.

Use it to research tokens, prepare trades, manage positions, and get product help in plain language.

Every trade is prepared for your review. Nothing executes without your approval.

See: [AI Assistant](../ai-assistant/ai-assistant.md).

</details>

### Wallet and Security

<details>

<summary>Is FatCat Bot non-custodial?</summary>

Yes. Fully non-custodial.

Your private key is generated inside a hardware-isolated Trusted Execution Environment (TEE).

It is immediately split into two encrypted shares.

The full key is never stored by anyone.

Neither FatCat nor Privy can access your private key.

Only your authenticated session can authorize transactions.

</details>

<details>

<summary>What is Privy?</summary>

Privy is the wallet infrastructure provider that generates and secures your embedded Solana wallet.

In simple terms, your private key is split into pieces and locked inside secure hardware. No single party, not FatCat and not Privy, ever holds the full key. Even if FatCat were hacked, your funds stay safe.

Privy is SOC 2 Type II certified and independently audited by Cure53, Zellic, and Doyensec.

</details>

<details>

<summary>Does FatCat have access to my private key?</summary>

No.

FatCat does not see, store, transmit, or handle your private key in any form at any point.

FatCat’s only role is to prepare transactions for you to review and approve.

All key management and signing happens inside Privy’s hardware-isolated environment, completely separate from FatCat’s systems.

</details>

<details>

<summary>Does Privy have access to my private key?</summary>

No.

Privy’s architecture is specifically designed so that even Privy’s own engineers cannot access your full private key.

The key only exists in its complete form inside the Trusted Execution Environment for the brief moment of signing, and is wiped immediately after.

</details>

<details>

<summary>Can I export my private key?</summary>

Yes. It is highly recommended that you export and store your private key.

You can export your full private key at any time through Privy’s secure environment.

The export happens in Privy’s isolated modal on a separate domain from FatCat.

FatCat never sees the key during this process.

Once exported, you can import it into Solflare, Backpack, or any Solana wallet.

</details>

<details>

<summary>What if I lose access to my email?</summary>

If you lose access to the email you used to sign in, contact Privy support for account recovery options.

We strongly recommend exporting and backing up your private key as a precaution.

</details>

<details>

<summary>What login methods are supported?</summary>

In Telegram’s built-in browser, email and SMS are supported.

Social logins like Google or Apple require pop-up windows that Telegram’s browser does not support.

</details>

### Trading

<details>

<summary>What is Jupiter?</summary>

Jupiter is Solana’s leading DEX aggregator and on-chain program provider. FatCat uses Jupiter for swaps, limit orders, DCA, and Jupiter Perps.

FatCat also supports GMTrade for broader Perps market coverage. Venue fees vary by feature. See [Fee Structure](../fees-and-rewards/fee-structure.md) for a breakdown of what each party charges.

</details>

<details>

<summary>Can I swap any token for any other token?</summary>

Yes.

FatCat supports swapping any Solana SPL token for any other Solana SPL token, as long as both have liquidity on a supported pool.

</details>

<details>

<summary>What tokens can I trade?</summary>

Any Solana SPL token that has liquidity on Jupiter.

See [Supported Tokens](../tokens/supported-tokens.md) for more details.

</details>

<details>

<summary>How do fees work?</summary>

FatCat charges a small fee on each trade.

Jupiter or GMTrade may also charge separate venue fees depending on the feature.

See [Fee Structure](../fees-and-rewards/fee-structure.md) for a full breakdown.

</details>

<details>

<summary>What is the minimum trade amount?</summary>

There is no hard minimum, but very small trades may not be practical due to Solana network fees and minimum output amounts.

</details>

### Limit orders and DCA

<details>

<summary>What’s the difference between a swap and a limit order?</summary>

Swaps execute immediately at the best available route.

Limit orders wait until price hits your target.

* [Limit Orders](../trading/limit-orders.md)
* [Swaps](../trading/swaps/)

</details>

<details>

<summary>What is DCA?</summary>

DCA splits one trade into smaller time-scheduled trades.

See: [DCA Orders](../trading/dca-orders/).

</details>

<details>

<summary>Can I cancel a limit order or DCA?</summary>

Yes.

Click the **Active Limit Orders** button to view and cancel limit orders. Click the **Active DCA Orders** button to cancel DCA orders.

Quick links:

* [Managing limit orders](../trading/limit-orders.md#managing-limit-orders)
* [Active DCA Orders](../trading/dca-orders/active-dca-orders.md)

</details>

<details>

<summary>What happens to my limit orders and DCA if I’m offline or logged out?</summary>

They keep running.

Limit orders and DCA orders are placed on-chain through Jupiter, so they execute automatically whether you’re online, logged out, or have your phone off.

You don’t need to stay connected for your orders to fill.

</details>

### Perps (leveraged trading)

<details>

<summary>What are Perps?</summary>

Perpetual Futures (Perps) let you trade long or short with leverage across Jupiter and GMTrade venues.

You can go long (bet on price going up) or short (bet on price going down).

</details>

<details>

<summary>Are Perps risky?</summary>

Yes.

Perps carry significant risk, especially at high leverage.

You can lose your entire position.

Use stop losses and trade responsibly.

</details>

<details>

<summary>How do Perps work?</summary>

Perps let you trade on price going up (long) or down (short) with leverage.

You deposit collateral, and the selected venue opens a leveraged position on your behalf. Profits and losses are settled by the venue when you close the trade.

Three things to understand before you trade:

* **Collateral** — the funds you deposit to back the position.
* **Leverage** — how large your position is relative to your collateral. Higher leverage means higher risk.
* **Liquidation** — if the market moves far enough against you, your position is force-closed and you lose all the collateral you deposited.

</details>

<details>

<summary>What collateral do I need?</summary>

It depends on venue and entry flow.

**Opening a position with the Telegram bot**

| Position type | Required collateral                           |
| ------------- | --------------------------------------------- |
| Long          | The token you’re longing (SOL, wBTC, or wETH) |
| Short         | USDC                                          |

**Opening a position with the web app or AI assistant**

| Position type | Required collateral            |
| ------------- | ------------------------------ |
| Long or Short | USDC, wBTC, wETH, USDT, or SOL |

</details>

<details>

<summary>What is leverage?</summary>

Leverage lets you open a position larger than your collateral.

Your **notional size** equals collateral × leverage. For example, $100 collateral at 10x leverage equals $1,000 notional size.

It multiplies both gains and losses. A 10% move against you on a 10x position can wipe your collateral entirely.

Start low.

</details>

<details>

<summary>What is liquidation?</summary>

Liquidation happens when the loss on your notional size equals your deposited collateral. At that point, the protocol force-closes your trade and you lose all the collateral you deposited.

Every position shows a liquidation price when you open it. Set a stop loss above that price.

</details>

<details>

<summary>What is a Stop Loss (SL)?</summary>

A stop loss automatically closes your position if the price reaches a level you set, limiting your loss before it reaches liquidation.

Set it between your entry price and your liquidation price. For longs, that means above liquidation. For shorts, below liquidation.

Example: long SOL at $150, liquidation at $120, stop loss at $135. If SOL drops to $135, the position closes automatically.

</details>

<details>

<summary>What is a Take Profit (TP)?</summary>

A take profit automatically closes your position when price hits your target, locking in your gains.

Example: long SOL at $150, take profit at $200. When SOL hits $200, the trade closes and profit goes to your wallet.

</details>

<details>

<summary>Why is my collateral and leverage slightly different from what I set?</summary>

This is normal.

Network fees apply, and venue fees can change your effective collateral slightly when the position opens.

Jupiter charges a fixed opening fee. GMTrade uses per-market fees that are shown at approval.

Your notional size stays aligned with what you set. The approval screen shows the live collateral, leverage, and fees before you sign.

</details>

### Fees

<details>

<summary>What fees do I pay?</summary>

You may pay:

* Network fees (Solana).
* Trading or routing fees, depending on the feature.

Full breakdown: [Fee Structure](../fees-and-rewards/fee-structure.md).

</details>

<details>

<summary>Why do I see a fee even if I cancel or the trade fails?</summary>

{% hint style="warning" %}
**Fees can be lost on failed or cancelled trades.** Some fees are charged **upfront** or **at approval** and are **non-refundable**, even if execution fails or you cancel the order.
{% endhint %}

Common cases:

* **Network fees (Solana):** paid when a transaction is sent, even if it fails.
* **Market swaps:** FatCat fee is charged upfront.
* **Limit/DCA:** FatCat fee is charged upfront. Jupiter is charged at fill or per swap.
* **Perps:** fees can be charged at approval and may be non-refundable.

Full breakdown: [Fee Structure](../fees-and-rewards/fee-structure.md).

</details>

### Telegram and support

<details>

<summary>Does Telegram give the bot access to my wallet?</summary>

No. Telegram is just the chat UI.

Wallet access is controlled by you.

</details>

<details>

<summary>I can buy a token but can’t sell it. Why?</summary>

Common causes:

* The token has transfer restrictions.
* Liquidity is too thin to exit at your size.
* The pool changed fast while you were selling.

If you’re stuck holding a token you can’t sell, try:

* **Retry the sell** — sometimes a second attempt goes through.
* **Wait 5–10 minutes** and try again — liquidity and conditions can change.
* **Reduce the sell amount** — selling a smaller portion may succeed.
* **Increase slippage tolerance** — a wider slippage can help in thin pools.

Read: [Trade Safely](../safety-and-security/trade-safely.md).

</details>

<details>

<summary>Will support DM me first?</summary>

Assume unsolicited DMs are scams.

Only trust support links you open yourself.

Read: [Avoiding Scams](../safety-and-security/avoiding-scams.md).

</details>

<details>

<summary>Where do I get help?</summary>

Use `🔔 Help` in the bot.

Or start here: [Help](../help-and-policies/help.md).

</details>

<details>

<summary>What should I include when I ask for help?</summary>

Share enough to debug, without sharing secrets.

Include:

* The feature you used (swap, limit, DCA, Perps).
* What step failed (connect, sign, pending, filled, etc.).
* A transaction signature (if one exists).
* A screenshot of the error, if you can.

Never share your seed phrase or private key.

</details>

{% hint style="info" %}
FatCat can’t reverse transactions.\
On-chain trades are final once confirmed.
{% endhint %}

### Troubleshooting

<details>

<summary>The sign-in page is not loading.</summary>

Make sure the page is opening inside Telegram’s built-in browser.

If you are having issues, try closing and reopening the bot, or clearing Telegram’s WebView cache in your device settings.

</details>

<details>

<summary>I did not receive a verification code.</summary>

Check your spam/junk folder for email codes.

For SMS, make sure you entered your phone number with the correct country code.

Wait at least 60 seconds before requesting a new code.

</details>

<details>

<summary>My session expired.</summary>

Tap Sign In again to re-authenticate.

Your wallet and funds are not affected by session expiry.

</details>

<details>

<summary>My transaction failed.</summary>

Common reasons for failed transactions:

* Insufficient SOL for network fees.
* High slippage — the token price moved too far during execution. Try increasing your slippage tolerance.
* Low liquidity — the token does not have enough liquidity on Jupiter for your trade size.
* Network congestion — Solana can experience temporary congestion. Wait a moment and try again.

</details>

<details>

<summary>I sent funds to the wrong address.</summary>

Transactions on Solana are irreversible.

FatCat cannot recover funds sent to the wrong address.

Always double-check addresses before sending.

</details>

### Withdraw

<details>

<summary>How do I withdraw funds?</summary>

Use the **Send** function, available in the Telegram bot and in the FatCat Web App.

Enter a destination Solana wallet address, select the token and amount, then confirm. Funds go directly on-chain.

See: [Send](../fatcat-bot-telegram/supporting-features/send.md).

</details>
