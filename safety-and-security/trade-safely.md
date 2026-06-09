---
description: Protect your wallet, verify tokens, and avoid common trading mistakes.
icon: shield-check
---

# Trade Safely

{% include "../.gitbook/includes/security-warning-support.md" %}

### Protect your wallet

* Keep your private key and seed phrase safe. Do not share either with anyone.
* Lock your phone and wallet app with a passcode or biometrics.
* Review every wallet prompt before you approve and sign.
* Disconnect sites you don’t recognize.

### Verify what you’re trading

* Confirm the token address (mint/contract) from an official source.
* Watch for copycat tokens with the same name or ticker.
* Review for price impact before you submit.

#### Verify it is an SPL token

Paste the mint address into a trusted Solana explorer and confirm it’s an SPL token.

* [https://explorer.solana.com](https://explorer.solana.com)
* [https://solscan.io](https://solscan.io)
* [https://solana.fm](https://solana.fm)

#### Token verification checklist

Use this before any first trade on a token.

* [ ] Mint address matches the official token you wish to trade.
* [ ] You’re trading the right asset for the right chain (Solana SPL mint).
* [ ] Name and ticker match.
* [ ] Liquidity is real and sufficient for your size. Expect slippage on thin pools.
* [ ] Volume is non-trivial. Dead pools are hard to exit.

See also: [Where to Find Tokens](../tokens/where-to-find-tokens.md) and [How Tokens Work](../tokens/how-tokens-work.md).

### If something feels off

{% stepper %}
{% step %}
### Stop and don’t sign

Cancel the transaction. Close the site or bot flow.
{% endstep %}

{% step %}
### Move funds to safety

If you suspect compromise, transfer remaining funds to a fresh wallet.
{% endstep %}

{% step %}
### Check what you connected

Review recent apps you used. Disconnect anything unfamiliar.
{% endstep %}
{% endstepper %}

For common patterns like fake token pages, rugs, and impersonators, see [Avoiding Scams](avoiding-scams.md).
