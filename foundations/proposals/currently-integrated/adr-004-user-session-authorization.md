---
description: >-
  With the increasing concerns around data privacy and security, it is crucial
  to develop a solution that ensures the confidentiality of user information
  while providing a seamless and user-friendly exp
---

# ADR-004: User Session Authorization

## Context

With the increasing concerns around data privacy and security, it is crucial to develop a solution that ensures the confidentiality of user information while providing a seamless and user-friendly experience.

The proposed solution for encrypted and anonymous PassKeys involves two user journeys: registering new users and authenticating existing users. During registration, users provide necessary information and generate a secure Webauthn credential anonymously linked to their account.

Basic profile information can be stored as encrypted data. For authentication, the Webauthn credential is auto-filled based on a registered session, providing a seamless experience. The service owner covers the authentication fee, and successful authentication results in a record stored on the chain for auditing and added security.

***

## O**bjective**

* Simplify Login experience with device native biometrics
* Compute Graph based relations for Zero-Knowledge elements and DIDs to ensure privacy
* Enable a truly decentralized system at the point of device, to service, to blockchain node.

***

## Sequence Methods

### 1. Registering New Users

If a valid registration request is sent, the token reward is minted for all parties of the Account Generation exchange.

* Options and Minimum accepted identifiers queried from Services
* User generates a Webauthn credential which is anonymously points to the users account
* User can store basic profile info as encrypted data when requested by services

### 2. Authenticating Existing Users

Upon successful authentication a New record of the event is stored on chain with an encrypted fingerprint and the account which was authenticated. The Service owner is responsible for paying the _Authentication Fee_.

* Client auto-fills webauthn credential based off previously registered session.
* Manager of the Service Record requesting authentication pays standard fees.

***

## Economic Impact

### Network Fees

<table><thead><tr><th></th><th width="115">Fees</th><th width="172">Sender</th><th>Receiver</th></tr></thead><tbody><tr><td>Lookup User Identifier existence in Zero-knowledge Accumulator</td><td>SNR 0.5</td><td>Service Owner</td><td>Validator</td></tr><tr><td>Verify a Signature</td><td>SNR 0.1</td><td>Service Owner</td><td>Validator</td></tr></tbody></table>

### Staking Incentives

| Action                   | Minimum Delegation | Unlock Period |
| ------------------------ | ------------------ | ------------- |
| Persisting a Username    | USNR 200,000,000   | 30 Days       |
| Elevate Developer Access | USNR 500,000,000   | 12 Months     |

***

## Implementation

### API Methods

| Summary                     | Method | Endpoint        |
| --------------------------- | ------ | --------------- |
| Query for an Identity       | GET    | /core/identity/ |
| Send a transaction on-chain | POST   | /core/identity/ |

***

## Status

This proposal is **under development** by the core Sonr Team.

| Development Phase | Testnet |
| ----------------- | ------- |
| Target Completion | Q1 2024 |

***
