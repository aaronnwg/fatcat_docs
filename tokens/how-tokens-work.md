# How Tokens Work

### Token basics on Solana

* **Token accounts:** balances are stored in on-chain token accounts. Receiving a token for the first time may create one, which costs a little SOL.
* **Authorities:** a **mint authority** can create more supply; a **freeze authority** can freeze accounts. If a mint authority still exists, supply can increase at any time.
* **The mint address is the real identity:** names, tickers, and logos can be copied or misleading.
* **Wrapped SOL (wSOL):** SOL is Solana's native coin, not an SPL token. Many pools trade against wSOL, a 1:1 wrapped version — wrapping changes format, not value.

### Metrics that matter

* **Price** — the current rate, usually in SOL or USDC; can change fast.
* **Liquidity** — how much is available to trade. Lower liquidity means more slippage and price impact, especially on larger trades.
* **Volume** — how much has traded in a window.
* **Market cap** — an estimate (`price × circulating supply`); treat as approximate.

### Supply

* **Total vs circulating supply:** total is everything minted minus burned; circulating is what's actually available (locked or vested tokens may not circulate).
* Projects can mint (increase) or burn (reduce) supply, which can affect price.

{% hint style="warning" %}
USDC and other stablecoins target ~$1 but carry issuer risk — some can freeze funds at the token level.
{% endhint %}
