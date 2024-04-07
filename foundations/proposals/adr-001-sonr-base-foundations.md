---
description: >-
  Sonr is a peer-to-peer identity and asset management system that leverages DID
  documents, Webauthn, and IPFS.
---

# ✔️ ADR-001: Sonr Base Foundations

## Abstract

**Sonr is a peer-to-peer identity and asset management system that leverages DID documents, Webauthn, and IPFS — providing users with a secure, user-friendly way to manage their digital identity and assets.**

Sonr is a Cosmos powered blockchain which is powered by a TenderMint validation mechanism. The default consensus for TenderMint is DPoS and works with our current ABCI implementation for Transaction Verification.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Sonr Holistic Authentication Feature Set</p></figcaption></figure>

***

## Protocol Economics

On Sonr there are two tokens which operate within protocols and execution.

| SNR                                                          | USNR                                                                                             |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| Used for paying for operations provided on the Sonr network. | Used for staking claim in the network for elevated permissions and calling authorized operations |
| $R(A)=1                                                      | 1 SNR = 1,000,000 uSNR                                                                           |

_Coin age is irrelevant. All coins that are mature will add the same staking weight — resulting in stable, consistent interest only for active wallets and only with small inputs._

### Value-Demand Relationship

The **Demand** is rooted from participation in the governance process, determining upgrades to the protocol or allocation of resources, and **supply** is the result of the tokens eligible to participate in the governance process.

$$
\text{Token Price (SNR)} = \text{Fundamental Value} + \text{Token Specific Non-Fundamentals} + \text{Market/Industry Non-Fundamentals}
$$

The **price** of a token is the exchange rate of the token for fiat. The **value** of the token can be modeled in terms of fundamental demand drivers and effective supply. The **demand** of the token is driven by the **property rights granted by the token**, and the effective **supply** is driven by the **number of tokens to which a specific set of rights are granted**.

### Utilized Blockchain Modules

| Module Name     | Description                                                            |
| --------------- | ---------------------------------------------------------------------- |
| `x/bank`        | Manages token minting and cross-chain asset deposits                   |
| `x/capability`  | Differentiates between various account addresses                       |
| `x/gov`         | Establishes governance guidelines for operator nodes                   |
| `x/group`       | Enables on-chain multi-signature accounts for organizations            |
| `x/ibcaccounts` | Leverages IBC Host/Controller Accounts across chains                   |
| `x/ibctransfer` | Provides bridge-less transfers natively for accounts                   |
| `x/identity`    | Manages identity primitives native to the Sonr blockchain              |
| `x/oracle`      | Handles cross-chain token deposits and price feeds                     |
| `x/permissions` | Manages available permissions services can request from accounts       |
| `x/service`     | Manages service record operations, validations, reporting, and gateway |
| `x/slashing`    | Facilitates actions against bad actors on the network                  |
| `x/upgrade`     | Enables software binary upgrades across nodes                          |
| `x/wasm`        | Allows deployment of Rust smart contracts to the Sonr network          |

## Network Governance

Establishing fundamental value via governance incorporates seven elements of economic design:

1. **Scope of Decisions**
2. **Stakeholders**
3. **Policy Research & Development**
4. **Proposal Process**
5. **Information Distribution Systems**
6. **Decision Making Procedures**
7. **Implementation & Property Rights**

### **Stakeholder Roles & Responsibilities**

| General Public                  | Sonr Treasury                      | Organizations                  | Node Operators                        |
| ------------------------------- | ---------------------------------- | ------------------------------ | ------------------------------------- |
| Vote on validator selection     | Propose/vote on new Grant themes   | Propose new permission types   | Propose and vote on validators        |
| Vote on software upgrades       | Propose and Vote Software Upgrades | Propose and vote on validators | Propose and vote new permission types |
| Report Validators/Organizations | Jail Validators and Organizations  | Vote on Software upgrades      | Propose and Vote Software Upgrades    |

### Governance Rollout Timeline

<table data-card-size="large" data-view="cards" data-full-width="false"><thead><tr><th>Stage</th><th>Objective</th><th>Actions</th></tr></thead><tbody><tr><td><strong>1) Establish Community</strong></td><td>Build a robust community of engaged token holders.</td><td><ol><li>Incentivize stake-holding and participation.</li><li>Partner with DeFi projects and blockchain services.</li></ol></td></tr><tr><td><strong>2) Polling System</strong></td><td>Initiate a preliminary system for community feedback.</td><td><ol><li>Implement a token-weighted polling system.</li><li>Enable community submissions and voting on improvements.</li></ol></td></tr><tr><td><strong>3) On-Chain Execution</strong></td><td>Launch an executable code-based governance framework.</td><td><ol><li>Introduce majority rule voting.</li><li>Analyze and incorporate community proposals after assessment.</li></ol></td></tr><tr><td><strong>4) Subsidies and Rewards</strong></td><td>Promote proposals for grants and rewards allocation.</td><td><ol><li>Allow community proposals for grants.</li><li>Use community voting to select grant recipients.</li></ol></td></tr><tr><td><strong>5) Technical Upgrades</strong></td><td>Maintain and enhance platform security and functionality.</td><td><ol><li>Conduct security and economic audits.</li><li>Update subsidies, rewards, and accept technical proposals.</li></ol></td></tr><tr><td><em><strong>Governed Maintenance</strong></em></td><td>Ensure regulatory c<em>ompliance with</em> <a data-footnote-ref href="#user-content-fn-1"><em>Wyoming DUNA</em></a><em>.</em></td><td><ol><li>Maintain polling-based system in Motor Nebula Widget.</li><li>Focus on pricing, security, and bug fixes in proposals.</li></ol></td></tr></tbody></table>

[^1]: The Wyoming DAO Supplement (DUNA) is a legal framework that allows Decentralized Autonomous Organizations (DAOs) to operate as limited liability companies (LLCs) in the state of Wyoming. It goes into effect [**July 2024**](https://www.wyoleg.gov/2024/Introduced/SF0050.pdf).
