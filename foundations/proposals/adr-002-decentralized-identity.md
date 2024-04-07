---
description: >-
  The x/identity module is responsible for the management of DIDDocuments
  on-chain and resolution of private user identifiers off-chain.
---

# ✔️ ADR-002: Decentralized Identity

## Context

Sonr aims to set a new standard in digital identity by aligning with W3C specifications for Decentralized Identifiers (DIDs). The current system's reliance on third-party identification and seed-phrases for wallet onboarding presents privacy risks and usability challenges. This proposal aims to eliminate these issues by enhancing our **`x/identity`** module.

## O**bjective**

* Enforce Compliance by implementing Decentralized Identifiers from W3C
* Prevent Applications and Services from associating 3rd-party identification with wallets
* Eliminate cumbersome onboarding by removing seed-phrases

***

## Sequence Methods

#### 1. Passkey Registration on _Verified Domains_

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Service-Proxied Registration using on-chain Record</p></figcaption></figure>

#### 2. Persisting Keyshares over _Decentralized Storage Provider_

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Restricting Access to provisioned users using IPFS Encrypted Vaults</p></figcaption></figure>

***

### Keyshare Mapping

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>2 Party DKLS MPC</p></figcaption></figure>

| Term           | Definition                                                                                  |
| -------------- | ------------------------------------------------------------------------------------------- |
| Alice          | Represents encrypted data stored on-chain and backed up in IPFS.                            |
| Bob            | Encrypted by a Zero Knowledge (zk) accumulator using traditional user-provided identifiers. |
| Pub            | Public information or public key.                                                           |
| SecData        | Secret data or private key information.                                                     |
| Curve          | Details about the cryptographic curve used.                                                 |
| Keyshare       | A fragment of a cryptographic key.                                                          |
| DID Controller | The controlling entity that interacts with the keyshares from both Alice and Bob.           |

## Economic Impact

### Staking Incentives

| Action                   | Minimum Delegation | Unlock Period |
| ------------------------ | ------------------ | ------------- |
| Persisting a Username    | USNR 200,000,000   | 30 Days       |
| Elevate Developer Access | USNR 500,000,000   | 12 Months     |

***

## Implementation

### Supported Methods

`did:idx`

***

## Status

This proposal is **under development** by the core Sonr Team.

| Development Phase | Testnet |
| ----------------- | ------- |
| Target Completion | Q4 2023 |
