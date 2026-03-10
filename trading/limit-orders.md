# Limit Orders

Limit orders let you set a target price for buying or selling a token.

FatCat monitors the market and executes the trade when your target is hit.

Limit orders stay active on-chain until filled, cancelled, or expired.

FatCat places limit orders on **Jupiter’s limit order book**.

Limit orders are available in both the FatCat Telegram bot and the FatCat Mobile App.

### Before you start

* Verify the token mint address from a trusted source.
* Keep extra SOL for network fees.
* Expect the market to move. A fill is never guaranteed.

See also: [Trade Safely](https://docs.fatcatbot.io/safety-and-security/trade-safely) and [Where to Find Tokens](https://docs.fatcatbot.io/tokens/where-to-find-tokens).

### What you can do

* **Buy:** swap **SOL → token** when your trigger price hits.
* **Sell:** swap **token → SOL** when your trigger price hits.

### Where to find it

You’ll see **Limit Order** inside the normal buy/sell flows.

You can manage your orders from the bot’s **Main Menu**.

### Fees

Limit orders include FatCat fees and Jupiter program fees.

* **FatCat fee:** **1%** (charged upfront when you place the order)
* **Jupiter fee:** **0.1%** (charged only if the order fills)
* **Solana network fees:** paid for the on-chain transactions

For the full breakdown, see [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

### How execution works

When you place a limit order:

* An on-chain order account is created for your wallet.
* Funds are escrowed in Jupiter’s limit order program for that order.
* Keeper services watch the chain for fill conditions.
* When your price is reachable, a keeper submits the fill transaction.
* Fill behavior depends on available liquidity at your price.

### Create a limit order

#### Setting a limit order (in FatCat Bot)

1. Start a buy or sell flow.
2. Tap the **Limit Order** button.
3. Enter your target limit price.
4. Confirm, then review and approve.

### What happens after you confirm

* **Order lifetime:** active until filled or cancelled.
* **Funds custody:** funds are held in a program-owned vault for the order.
* **Fill behavior:** depends on available on-chain liquidity at your price.
* **Settlement:** when filled, output assets go to your wallet.

### Managing limit orders

* View active limit orders (Main Menu).
* View completed/cancelled limit orders (Main Menu).
* You can also view and manage them on Jupiter: <https://jup.ag/limit>

### Troubleshooting

If an order looks “stuck”, it’s usually one of these:

* Price never reaches your target on-chain.
* Liquidity is too thin at your target price.
* Price moves through your target too quickly.

{% hint style="warning" %}
Fast markets can skip your level. A fill is never guaranteed.
{% endhint %}
