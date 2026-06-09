---
description: Non-custodial Solana trading in Telegram.
icon: wreath-laurel
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
metaLinks:
  alternates:
    - /broken/spaces/yE16Xb3IemPxJWydtPOj/pages/LThc2RqOxBKU56Qt3TMy
---

# Welcome

FatCat Bot is a non-custodial Telegram bot for trading Solana tokens and Perps.

Place spot orders, limit orders, automate buys with DCA, and trade Perps. You stay in control of your funds the whole time.

{% include ".gitbook/includes/security-warning-support.md" %}

### Overview

#### What is FatCat Bot?

FatCat Bot runs inside Telegram. You sign in and connect or create a secure Solana wallet. No browser extensions. No separate apps. No seed phrases for embedded wallets.

You can:

* Swap Solana tokens at market price.
* Place limit orders.
* Trade Perpetual Futures (Perps).
* Automate buys and sells with DCA.
* Send tokens to any Solana wallet.

#### How it works

FatCat Bot supports Privy embedded wallets and wallet connection to keep trading seamless. When you sign in, you can create a Privy Solana wallet or connect an existing wallet. If you create a Privy wallet, your private key is created inside a hardware-isolated Trusted Execution Environment (TEE), immediately split into encrypted shares using Shamir's Secret Sharing with a 2-of-2 share set, and never stored as a whole. No one can access your full private key: not FatCat, not Privy, not anyone. Only you, authenticated through your email or phone, can authorize transactions.

When you set up a swap, limit order, DCA order, or Perp position, FatCat prepares the transaction and you approve it directly inside the app. Nothing executes without your explicit approval.

This means:

* FatCat never has access to your private keys. Not during setup, not during signing, not ever. FatCat does not see, store, transmit, or handle your private key in any form.
* Privy cannot access your private keys either. Keys exist only momentarily inside the TEE during signing, then are immediately wiped. Even Privy’s own engineers cannot access what runs inside the enclave.
* Only you can authorize transactions. Your authenticated session (email or phone verification) is the only way to trigger signing.
* FatCat cannot move funds on your behalf.
* Your assets stay in your wallet until you approve.
* You can export your private key at any time through Privy’s secure, isolated environment. FatCat has zero visibility into the export process.

#### Core features

* **Spot trading:** swap any Solana token for any other Solana token.
* **Limit orders:** execute when a token hits your target price.
* **DCA (dollar cost averaging):** automate recurring buys or sells over time.
* **Perpetual Futures (Perps):** trade across Jupiter and GMTrade markets with leverage and risk controls. Set stop losses and take profits.
* **AI Assistant:** research tokens, prepare trades, manage positions, and get product help in plain language.
* **Send:** transfer tokens from your FatCat wallet to any Solana wallet.
* **FatCat Web App:** a dedicated web-based trading interface with live charts, swaps, limit orders, Perps, and portfolio management. Recommended for the best trading experience.

{% hint style="warning" %}
Perps are high risk, especially at high leverage.
{% endhint %}

#### Powered by Jupiter and GMTrade

FatCat Bot integrates with Jupiter for swaps, limit orders, DCA, and Jupiter Perps. FatCat also integrates with GMTrade for broader Perps market coverage. This keeps execution on-chain across supported venues.

#### What you’ll need

* A Telegram account.
* An email address or phone number (if you create an embedded wallet).
* SOL for network fees and trading.

#### Telegram commands vs buttons

FatCat works like most Telegram bots: you can use **buttons** or **slash commands**. Both routes end up in the same flows.

* **Buttons:** best for most users. They reduce typos and keep you on rails.
* **Commands:** faster if you already know what you want. Great for power users.

### Jump right in

* [Setting Up Your Wallet](overview/getting-started/setting-up-your-wallet.md): sign in and connect or create your embedded wallet.
* [Quick Start Guide](overview/quick-start-guide.md): fastest path to your first trade.
* [AI Assistant](ai-assistant/ai-assistant.md): trade and research in plain language.
* [Swaps](trading/swaps/): swap any Solana token for any other.
* [Market Buy & Market Sell](trading/swaps/market-buy-and-market-sell.md): step-by-step spot trading flow.
* [Limit Orders](trading/limit-orders.md): set a target price and let it fill.
* [DCA Orders](trading/dca-orders/): automate buys or sells over time.
* [Perps](trading/perps/): long/short with leverage and risk controls.
* [FatCat Web App](fatcat-web-app/fatcat-web-app.md): the recommended web trading interface.
* [Send](fatcat-bot-telegram/supporting-features/send.md): transfer tokens from your FatCat wallet to any Solana wallet.
* [Trade Safely](safety-and-security/trade-safely.md): avoid scams, verify mints, use a trading wallet.
* [Avoiding Scams](safety-and-security/avoiding-scams.md): common traps and how to spot them.
* [FAQ](overview/faq.md): quick answers and troubleshooting.
