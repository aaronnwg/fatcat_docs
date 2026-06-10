# FAQ

Common questions for trading with FatCat Bot. Need help inside Telegram? Use `🔔 Help`, or see [Help](https://docs.fatcatbot.io/help-and-policies/help).

{% hint style="warning" %}
Never share your seed phrase or private key. Assume unsolicited support DMs are scams.
{% endhint %}

### General

<details>
<summary>What is FatCat Bot?</summary>

A Solana trading app inside Telegram. Swap any Solana token, place limit orders, automate with DCA, and trade Perpetual Futures.
</details>

<details>
<summary>Do I need a separate wallet app?</summary>

No. FatCat uses Privy embedded wallets — your Solana wallet is created automatically when you sign in with your email. You can export the private key and import it into any wallet at any time.
</details>

### Wallet and security

<details>
<summary>Is FatCat non-custodial?</summary>

Yes. Your private key is generated inside a hardware-isolated Trusted Execution Environment and split into encrypted shares — the full key is never stored. Neither FatCat nor Privy can access it; only your authenticated session can authorize transactions.
</details>

<details>
<summary>Can I export my private key?</summary>

Yes, at any time — we recommend it. Once exported, import it into any Solana wallet.
</details>

<details>
<summary>What login methods are supported?</summary>

Email. Social logins need pop-ups Telegram's browser doesn't support.
</details>

### Trading

<details>
<summary>What tokens can I trade?</summary>

Any Solana SPL token with liquidity on a supported pool. See [Supported Tokens](https://docs.fatcatbot.io/tokens/supported-tokens).
</details>

<details>
<summary>Can I cancel a limit order or DCA?</summary>

Yes, from the bot menu or Mobile App. Remaining funds are returned; already-executed swaps and paid fees are not reversed.
</details>

<details>
<summary>I can buy a token but can't sell it. Why?</summary>

Usually transfer restrictions, thin liquidity, or a fast-moving pool. Try retrying, waiting a few minutes, reducing the amount, or increasing slippage. See [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely).
</details>

### Perps

<details>
<summary>What are Perps?</summary>

Perpetual Futures let you trade SOL, BTC, ETH, and other markets with leverage — long (price up) or short (price down). FatCat routes Perps through multiple venues (GMTrade, Jupiter, and Flash Trade).
</details>

<details>
<summary>How do Perps work?</summary>

You deposit collateral and the venue opens a leveraged position. Notional size = collateral × leverage. If the market moves far enough against you, the position is liquidated and you lose your collateral. Use stop losses and start with low leverage.
</details>

<details>
<summary>What collateral do I need?</summary>

It depends on the venue and direction, and is shown when you open the position. If you pay in a different token, a swap is bundled into the same transaction.
</details>

<details>
<summary>Why are my collateral and leverage slightly different from what I set?</summary>

Normal — opening fees are deducted from collateral when the position opens, so effective values shift slightly. Notional size stays as expected.
</details>

### Fees

<details>
<summary>What fees do I pay?</summary>

Solana network fees plus trading/routing fees depending on the feature. See [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).
</details>

<details>
<summary>Why a fee if I cancel or the trade fails?</summary>

Some fees are charged upfront or at approval and are non-refundable. Network fees are paid when a transaction is sent, even if it fails.
</details>

### Support & troubleshooting

<details>
<summary>Will support DM me first?</summary>

No — assume unsolicited DMs are scams. Only trust links you open yourself. See [Avoiding Scams](https://docs.fatcatbot.io/safety-and-security/avoiding-scams).
</details>

<details>
<summary>My transaction failed.</summary>

Common reasons: insufficient SOL for fees, slippage too tight, low liquidity, or network congestion. Adjust and retry.
</details>

<details>
<summary>I sent funds to the wrong address.</summary>

Solana transactions are irreversible and can't be recovered. Always double-check before sending.
</details>

<details>
<summary>How do I withdraw?</summary>

Use **Send**: enter a destination address, token, and amount, then confirm. See [Send](https://docs.fatcatbot.io/send).
</details>

{% hint style="info" %}
FatCat can't reverse transactions. On-chain trades are final once confirmed.
{% endhint %}
