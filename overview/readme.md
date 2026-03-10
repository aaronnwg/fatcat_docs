# Welcome

FatCat Bot is a self-custodial Telegram bot for trading Solana tokens and Perps.

Place spot orders, limit orders, automate buys with DCA, and trade Perps. You stay in control of your funds the whole time.

{% hint style="warning" %}
Never share your seed phrase or private key.\
FatCat support will never ask for them.
{% endhint %}

### Overview

#### What is FatCat Bot?

FatCat Bot runs inside Telegram. You sign in with your email, and a secure Solana wallet is created for you automatically. No browser extensions. No separate apps. No seed phrases.

You can:

* Swap Solana tokens at market price.
* Place limit orders.
* Trade leveraged Perpetual Futures (Perps).
* Automate buys and sells with DCA.

#### How it works

FatCat Bot uses Privy embedded wallets to keep your funds secure while making trading seamless. When you sign in for the first time, Privy generates a Solana wallet for you. Your private key is created inside a hardware-isolated Trusted Execution Environment (TEE), immediately split into encrypted shares using Shamir's Secret Sharing with a 2-of-2 share set, and never stored as a whole. No one can access your full private key: not FatCat, not Privy, not anyone. Only you, authenticated through your email or phone, can authorize transactions.

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
* **Perpetual Futures:** trade SOL, BTC, and ETH Perps with up to 250x leverage via Jupiter Perpetuals. Set stop losses and take profits.
* **FatCat Mobile App:** a dedicated web-based trading interface with live charts, swaps, limit orders, Perps, and portfolio management. Recommended for the best trading experience.

{% hint style="warning" %}
Perps are high risk, especially at high leverage.
{% endhint %}

#### Powered by Jupiter

FatCat Bot integrates with Jupiter's DEX and programs for swaps, limit orders, DCA, and Perpetual Futures. This grants you access to deep liquidity, optimized routing, and established infrastructure all through Telegram.

#### What you’ll need

* A Telegram account.
* An email address (for wallet setup).
* SOL for network fees and trading.

#### Telegram commands vs buttons

FatCat works like most Telegram bots: you can use **buttons** or **slash commands**. Both routes end up in the same flows.

* **Buttons:** best for most users. They reduce typos and keep you on rails.
* **Commands:** faster if you already know what you want. Great for power users.

### Jump right in

* [Setting Up Your Wallet](https://docs.fatcatbot.io/overview/getting-started/setting-up-your-wallet): sign in and create your embedded wallet.
* [Quick Start Guide](https://docs.fatcatbot.io/overview/quick-start-guide): fastest path to your first trade.
* [Swaps](https://docs.fatcatbot.io/trading/swaps): swap any Solana token for any other.
* [Market Buy & Market Sell](https://docs.fatcatbot.io/trading/swaps/market-buy-and-market-sell): step-by-step spot trading flow.
* [Limit Orders](https://docs.fatcatbot.io/trading/limit-orders): set a target price and let it fill.
* [DCA Orders](https://docs.fatcatbot.io/trading/dca-orders): automate buys or sells over time.
* [Perps](https://docs.fatcatbot.io/trading/perps): long/short with leverage and risk controls.
* [FatCat Mobile App](https://docs.fatcatbot.io/fatcat-mobile-app/fatcat-mobile-app): the recommended web trading interface.
* [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely): avoid scams, verify mints, use a trading wallet.
* [Avoiding Scams](https://docs.fatcatbot.io/safety-and-security/avoiding-scams): common traps and how to spot them.
* [FAQ](https://docs.fatcatbot.io/overview/faq): quick answers and troubleshooting.
