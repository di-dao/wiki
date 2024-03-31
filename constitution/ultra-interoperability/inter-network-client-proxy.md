---
description: >-
  The Sonr Highway serves as the "limbo state" for clients pending user
  authorization on-chain.
---

# Inter-Network Client Proxy

Sonr is introducing a groundbreaking feature called Intermediary Client Proxy, which revolutionizes the way users interact with their blockchain accounts. This innovative solution combines advanced cryptographic techniques with a user-friendly REST API gateway, providing a seamless and secure wallet experience without the need for additional browser extensions.

## The Challenge of Account Verification and Wallet Integration

In the realm of decentralized applications and blockchain technology, verifying the authenticity of user accounts while maintaining privacy and anonymity has been a significant challenge. Additionally, users often face the burden of installing and managing multiple browser extensions, such as MetaMask or Coinbase Wallet, to interact with their blockchain accounts.

Sonr recognizes the need for a solution that simplifies the account verification process and eliminates the reliance on third-party extensions. By leveraging zero-knowledge proofs and decentralized identifiers (DIDs), Sonr aims to provide users with a seamless and secure wallet experience.

## How Intermediary Client Proxy Works

Intermediary Client Proxy utilizes advanced cryptographic techniques to enable anonymous account verification and provide a full wallet interface through a REST API. Here's how it works:

1. **Zero-Knowledge Witness/Accumulator Pairs**: Sonr associates each user's blockchain account with a unique zero-knowledge witness/accumulator pair. These pairs allow users to prove the authenticity of their accounts without revealing sensitive information.
2. **Decentralized Identifiers (DIDs)**: Each user's blockchain account is linked to a decentralized identifier (DID). DIDs serve as a unique and verifiable identifier for the user's account, enabling resolveability and interoperability across different blockchain networks.
3. **REST API Gateway**: Sonr provides a REST API gateway that acts as an intermediary between the user and their blockchain account. This gateway exposes a full wallet interface, allowing users to perform various actions, such as sending transactions, managing assets, and interacting with smart contracts.
4. **Anonymous Account Verification**: When a user wants to access their wallet through the REST API gateway, they provide their zero-knowledge witness/accumulator pair. The gateway verifies the authenticity of the user's account using the provided proof, without requiring any additional personal information.
5. **Seamless Wallet Integration**: Once the user's account is verified, they can interact with their wallet seamlessly through the REST API. This eliminates the need for installing and managing browser extensions like MetaMask or Coinbase Wallet, providing a more user-friendly and accessible experience.

## Benefits of Intermediary Client Proxy

Intermediary Client Proxy offers several benefits to Sonr users:

1. **Enhanced Privacy**: By utilizing zero-knowledge proofs, Sonr allows users to verify the authenticity of their accounts without revealing sensitive information. This ensures that users can maintain their privacy while still proving ownership of their blockchain accounts.
2. **Simplified User Experience**: With the REST API gateway, users can interact with their wallets seamlessly without the need for additional browser extensions. This simplifies the user experience and reduces the friction associated with managing multiple extensions.
3. **Improved Accessibility**: Intermediary Client Proxy makes it easier for users to access and manage their blockchain accounts from various devices and platforms. By providing a standard REST API, Sonr enables developers to build applications that integrate with users' wallets effortlessly.
4. **Interoperability**: The use of decentralized identifiers (DIDs) allows for interoperability across different blockchain networks. Users can prove the authenticity of their accounts and interact with multiple blockchain ecosystems using a single identifier.

## Conclusion

Intermediary Client Proxy represents a significant advancement in account verification and wallet integration. By leveraging zero-knowledge proofs, decentralized identifiers, and a REST API gateway, Sonr provides users with a secure, private, and user-friendly way to interact with their blockchain accounts.

This feature aligns with Sonr's mission to empower users with control over their digital assets while promoting accessibility and ease of use. By eliminating the need for browser extensions and simplifying the account verification process, Sonr is paving the way for wider adoption of blockchain technology.

As Sonr continues to innovate and develop cutting-edge solutions, Intermediary Client Proxy demonstrates the project's commitment to providing users with the tools they need to navigate the decentralized landscape with confidence and convenience.
