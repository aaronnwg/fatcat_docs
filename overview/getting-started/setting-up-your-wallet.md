# Setting Up Your Wallet

FatCat Bot uses Privy embedded wallets. Your wallet is created automatically the first time you sign in.

### Create your wallet

1. Open FatCat and you will be prompted to sign in with your email.
2. Enter your email and the verification code in the secure page that opens.
3. Privy creates a Solana wallet and returns you, ready to trade.

{% hint style="info" %}
Only **email** login work in Telegram's browser. Social logins need pop-ups it doesn't allow.
{% endhint %}

### How it's secured

FatCat is fully non-custodial — only you can access your private key.

* Your key is generated inside a hardware-isolated Trusted Execution Environment (TEE) and immediately split into encrypted shares (the full key is never stored).
* To sign, the shares are briefly combined inside the TEE, then wiped from memory.
* Neither FatCat nor Privy can access your full key — only your authenticated session can trigger signing.

Privy is SOC 2 Type II certified and independently audited.

### Export your private key

You can export your full key at any time through Privy's secure modal, then import it into any Solana wallet. FatCat never sees it.

{% hint style="info" %}
We recommend exporting and backing up your key offline — it's your backup if you lose access to your email or phone.
{% endhint %}
