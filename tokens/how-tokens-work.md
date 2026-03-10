# How Tokens Work

### Token basics on Solana

#### Tokens live in token accounts

Each token balance is stored in a **token account** on-chain.

Most wallets use an **associated token account (ATA)** as the default.

#### Every action is an on-chain transaction

Creating a token account, swapping, and sending tokens all require SOL for fees.

If you receive a token for the first time, a token account may be created.

#### Authority controls matter

Many tokens have special authorities set at the mint level.

Common ones:

* **Mint authority:** can create more supply.
* **Freeze authority:** can freeze token accounts in some cases.

{% hint style="warning" %}
If a token still has a mint authority, supply can increase at any time.
{% endhint %}

#### Names and tickers are not the source of truth

The mint address is the token’s real identity.

Names, tickers, and logos come from metadata and lists.

They can be misleading or copied.

#### Wrapped SOL (wSOL)

SOL is Solana’s native coin, not an SPL token.

Many pools trade against **wSOL**, which is a 1:1 wrapped version of SOL.

Wrapping and unwrapping does not change value. It changes the token format.

### The metrics that matter

#### Price

The current exchange rate, usually quoted in SOL or USDC.

Price can change fast. This is normal in on-chain markets.

#### Liquidity

How much of the token is available to trade in pools.

Lower liquidity usually means:

* more slippage
* worse fills
* higher price impact on buys and sells

AMM pools reprice as you trade.

Bigger trades move the price more when liquidity is low.

#### Volume

How much has traded in a time window.

#### Market cap

An estimate of total value in circulation.

Common formula: `market cap = price × circulating supply`.

Treat market cap as an estimate. Supply and pricing sources can differ.

### Supply concepts

#### Mint

The token’s unique identifier on Solana.

Use the mint address to avoid copycat tokens.

See: [Where to Find Tokens](https://docs.fatcatbot.io/tokens/where-to-find-tokens).

#### Mints and burns

Projects can increase supply (mint) or reduce supply (burn).

This can affect price, but it’s not a guarantee.

#### Total supply vs circulating supply

**Total supply** is everything minted minus what has been burned.

**Circulating supply** is what’s actually available in the market.

Locked, vested, or treasury-held tokens may not be “circulating”.

#### Holders

The count of wallets holding the token.

More holders can mean broader distribution. It can also include bots.

### Stablecoins (USDC on Solana)

USDC on Solana is a USD-pegged stablecoin.

* `1 USDC` targets `~$1`
* Useful as a quote currency for trading
* Lower volatility than most tokens

{% hint style="warning" %}
Stablecoins also have issuer risk. Some stablecoins can freeze funds at the token level.
{% endhint %}
