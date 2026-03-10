# FAQ

Common questions for trading with FatCat Bot in Telegram.

### Start here (quick links)

{% columns %}
{% column %}
**Quick Start Guide**\
Fastest path to your first trade.

Go to: [Quick Start Guide](https://docs.fatcatbot.io/overview/quick-start-guide)

**Setting up your wallet**\
Create your embedded wallet and learn how approvals work.

Go to: [Setting Up Your Wallet](https://docs.fatcatbot.io/overview/getting-started/setting-up-your-wallet)
{% endcolumn %}

{% column %}
**Swaps (spot trading)**\
Market buy/sell basics, slippage, and failed swaps.

Go to: [Swaps](https://docs.fatcatbot.io/trading/swaps)

**Fees**\
What you pay, and when you pay it.

Go to: [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure)
{% endcolumn %}
{% endcolumns %}

### Jump to a section

* [General](#general)
* [Wallet and Security](#wallet-and-security)
* [Trading](#trading)
* [Limit orders and DCA](#limit-orders-and-dca)
* [Perps (leveraged trading)](#perps-leveraged-trading)
* [Fees](#fees)
* [Telegram and support](#telegram-and-support)
* [Troubleshooting](#troubleshooting)

Need help inside Telegram? Use `🔔 Help` in the bot.

Also see: [Help](https://docs.fatcatbot.io/help-and-policies/help).

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

FatCat Bot is free to start.

Fees are charged on trades.

See [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure) for details.

</details>

<details>

<summary>Do I need a separate wallet app?</summary>

No.

FatCat uses Privy embedded wallets.

Your Solana wallet is created automatically when you sign in with your email.

There is nothing to download or install.

</details>

<details>

<summary>Can I use my existing Solana wallet (Solflare, Backpack, etc.)?</summary>

FatCat uses Privy embedded wallets.

If you have funds in an existing wallet, transfer them to your FatCat wallet address to start trading.

You can also export your FatCat wallet’s private key and import it into any other wallet at any time.

</details>

<details>

<summary>What is the FatCat Mobile App?</summary>

The FatCat Mobile App is a web-based trading interface you can open directly from the bot menu.

It offers live charts, swaps, limit orders, Perps trading, and portfolio management in a visual interface.

It is the recommended way to trade for the best experience.

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

It uses hardware-isolated encryption (AWS Nitro Enclaves) and key sharding (Shamir’s Secret Sharing, 2-of-2 share set) to ensure that no single party can access your private key.

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

Yes.

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

<summary>Can I swap any token for any other token?</summary>

Yes.

FatCat supports swapping any Solana SPL token for any other Solana SPL token, as\
long as both have liquidity on Jupiter.

</details>

<details>

<summary>What tokens can I trade?</summary>

Any Solana SPL token that has liquidity on Jupiter.

See [Supported Tokens](https://docs.fatcatbot.io/tokens/supported-tokens) for more details.

</details>

<details>

<summary>How do fees work?</summary>

FatCat charges a small fee on each trade.

Jupiter may also charge separate fees depending on the order type.

See [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure) for a full breakdown.

</details>

<details>

<summary>What is the minimum trade amount?</summary>

There is no hard minimum, but very small trades may not be practical due to Solana network fees and minimum output amounts.

</details>

<details>

<summary>Can I cancel a limit order or DCA?</summary>

Yes.

You can cancel active limit orders and DCA orders from the bot menu or the FatCat Mobile App.

Any remaining funds are returned to your wallet.

</details>

### Limit orders and DCA

<details>

<summary>What’s the difference between a swap and a limit order?</summary>

Swaps execute immediately at the best available route.

Limit orders wait until price hits your target.

* [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders)
* [Swaps](https://docs.fatcatbot.io/trading/swaps)

</details>

<details>

<summary>What is DCA?</summary>

DCA splits one trade into smaller time-scheduled trades.

See: [DCA Orders](https://docs.fatcatbot.io/trading/dca-orders).

</details>

<details>

<summary>Can I cancel a limit order or DCA?</summary>

Yes.

Click the "Active Limit Orders" button to view and cancel limit orders, and click the "Active DCA Orders" button to cancel DCA orders.

Quick links:

* [Managing limit orders](https://docs.fatcatbot.io/trading/limit-orders#managing-limit-orders)
* [Active DCA Orders](https://docs.fatcatbot.io/trading/dca-orders/active-dca-orders)

</details>

### Perps (leveraged trading)

<details>

<summary>What are Perps?</summary>

Perpetual Futures (Perps) let you trade SOL, BTC, and ETH with leverage up to 250x via Jupiter Perpetuals.

You can go long (bet on price going up) or short (bet on price going down).

</details>

<details>

<summary>Are Perps risky?</summary>

Yes.

Perps carry significant risk, especially at high leverage.

You can lose your entire position.

Use stop losses and trade responsibly.

</details>

<br>

### Fees

<details>

<summary>What fees do I pay?</summary>

You may pay:

* Network fees (Solana).
* Trading / routing fees, depending on the feature.

Full breakdown: [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

</details>

<details>

<summary>Why do I see a fee even if I cancel or the trade fails?</summary>

Some fees are charged **upfront** or **at approval**.

That can make them non-refundable, even if execution fails later.

Common cases:

* **Network fees (Solana):** paid when a transaction is sent, even if it fails.
* **Market swaps:** FatCat fee is charged upfront.
* **Limit/DCA:** FatCat fee is charged upfront. Jupiter is charged at fill / per swap.
* **Perps:** fees can be charged at approval and may be non-refundable.

Full breakdown: [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

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

Read: [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely).

</details>

<details>

<summary>Will support DM me first?</summary>

Assume unsolicited DMs are scams.

Only trust support links you open yourself.

Read: [Avoiding Scams](https://docs.fatcatbot.io/safety-and-security/avoiding-scams).

</details>

<details>

<summary>Where do I get help?</summary>

Use `🔔 Help` in the bot.

Or start here: [Help](https://docs.fatcatbot.io/help-and-policies/help).

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

For SMS, make sure you entered your with the correct country code.

Wait at least 60 seconds before requesting a new code.

</details>

<details>

<summary>My session expired.</summary>

Privy sessions can expire after a period of inactivity.

Tap Sign In again to re-authenticate.

Your wallet and funds are not affected by session expiry.

</details>

<details>

<summary>My transaction failed.</summary>

Common reasons for failed transactions:

* Insufficient SOL for network fees.
* High slippage - the token price moved too far during execution. Try increasing your slippage tolerance.
* Low liquidity - the token does not have enough liquidity on Jupiter for your trade size.
* Network congestion - Solana can experience temporary congestion. Wait a moment and try again.

</details>

<details>

<summary>I sent funds to the wrong address.</summary>

Transactions on Solana are irreversible.

FatCat cannot recover funds sent to the wrong address.

Always double-check addresses before sending.

</details>

<br>
