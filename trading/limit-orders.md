# Limit Orders

Limit orders let you set a target price to buy or sell a token. FatCat places them on Jupiter's on-chain limit order book, where they stay active until filled, cancelled, or expired. Available in the Telegram bot and the Mobile App.

### Before you start

* Verify the token mint address from a trusted source.
* Keep extra SOL for network fees.
* A fill is never guaranteed — the market may never reach your price.

### Fees

* **FatCat:** **0.1%**, charged upfront when you place the order.
* **Jupiter program fee:** only if the order fills. Plus Solana network fees.

See [Fee Structure](https://docs.fatcatbot.io/fees-and-rewards/fee-structure).

### Create a limit order

Start a buy or sell flow, tap **Limit Order**, enter your target price, then review and approve. Funds are escrowed on-chain and keepers fill the order automatically when your price is reachable; output assets go to your wallet. Manage orders from the Main Menu or on Jupiter at <https://jup.ag/limit>.

{% hint style="warning" %}
Fast markets can skip your level. A fill is never guaranteed.
{% endhint %}
