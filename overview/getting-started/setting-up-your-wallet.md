# Setting Up Your Wallet

FatCat Bot uses Privy embedded wallets.

Your wallet is created automatically when you sign in for the first time.

There is nothing to install.

### Creating your wallet

1\. Open FatCat Bot in Telegram and tap **Sign In**.

2\. A secure page opens inside Telegram’s built-in browser.

3\. Enter your email address.

4\. Enter the verification code that is sent to you.

5\. Privy creates a Solana wallet for you automatically.

6\. You are returned to the bot, ready to trade.


### Supported login methods in Telegram

Due to how Telegram’s built-in browser works, only **email** and **SMS** login are supported.

Social logins (Google, Apple, etc.) require pop ups that Telegram’s browser does not allow.

### How your wallet is secured

FatCat Bot is fully non-custodial.

No one has access to your private key except you.

Here is how it works:

1\. **Key generation:** Your private key is generated inside a Trusted Execution Environment (TEE), specifically AWS Nitro Enclaves. This is a hardware-isolated enclave. No software, no person, no engineer at Privy or FatCat can see what happens inside it.

2\. **Key sharding:** Immediately after generation, the key is split into two encrypted shares using Shamir’s Secret Sharing (2-of-2 share set). The full key is destroyed. It is never stored as a whole by anyone, anywhere.

3\. **Signing:** When you approve a transaction, both shares are temporarily brought together inside the TEE, the transaction is signed, and the key is wiped from memory immediately. The full key exists only for the brief moment of signing, only inside the hardware enclave, and only because you authenticated.

4\. **FatCat has zero access:** FatCat does not see, store, transmit, or handle your private key in any form, at any point, under any circumstances. FatCat’s role is limited to preparing transactions for you to review and approve.

5\. **Privy has zero access:** Privy’s architecture is specifically designed so that even Privy themselves cannot access your full private key. The key only exists inside the TEE, which is isolated from all external access including Privy’s own infrastructure.

6\. **Only you can sign:** Your authenticated session (verified through your email) is the sole mechanism that can trigger the signing process. Without your active authentication, nothing happens.

Privy is SOC 2 Type II certified and has been independently audited by Cure53, Zellic, and Doyensec.

### Approving transactions

When you place a trade, set a limit order, start a DCA, or open a Perp position:

1\. FatCat builds the transaction and shows you a summary.

2\. You review the details in the app.

3\. You tap to approve.

4\. Privy reconstructs your key momentarily inside the TEE, signs the transaction, and immediately wipes the key.

5\. The signed transaction is submitted to the Solana network.

FatCat never touches your private key at any point in this process.

### Exporting your private key

You own your wallet.

You can export your full private key at any time.

1\. Go to the wallet export option in the app.

2\. Privy opens a secure modal on their own domain (a separate origin from FatCat’s app).

3\. Your key is reconstructed inside Privy’s isolated environment.

4\. The key is displayed for you to copy.

5\. FatCat never sees it. The export happens entirely within Privy’s sandboxed iframe on a different origin. FatCat’s app cannot read, intercept, or access anything that happens in that modal.

Once exported, you can import the key into any Solana wallet.

{% hint style="info" %}
We recommend exporting and securely backing up your private key.

Store it offline in a safe location, just as you would a seed phrase.

This is your backup if you ever lose access to your email or phone.
{% endhint %}

### Who can access your private key?

| Party               | Can access your private key?                               |
| ------------------- | ---------------------------------------------------------- |
| You (authenticated) | Yes. You are the only one.                                 |
| FatCat              | No. Never. Under no circumstances.                         |
| Privy               | No. Their own architecture prevents it.                    |
| Privy engineers     | No. The TEE is hardware-isolated from all external access. |
| Anyone else         | No.                                                        |

### Difference from traditional wallets

| Category               | Traditional wallet (e.g. Phantom)                           | Privy embedded wallet                                                     |
| ---------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------- |
| Setup                  | Download an app/extension, create account, save seed phrase | Enter email/phone, receive a code, done.                                  |
| Key storage            | You hold the full key in the app.                           | Key is split into **2-of-2 shares** and secured with hardware encryption. |
| Who can access the key | You (via the wallet app).                                   | You (via authenticated session). Nobody else.                             |
| Signing                | Opens a separate app/extension for approval.                | Happens directly in the interface.                                        |
| Portability            | Tied to the wallet app.                                     | Export your key and use it anywhere.                                      |
| Device support         | May differ between mobile and desktop.                      | Same experience on every device.                                          |

<br>
