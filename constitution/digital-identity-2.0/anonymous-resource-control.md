---
description: >-
  Sonr combines DIDs, UCANs, and IPFS to enable pseudonymous data access
  control, empowering users with privacy and sovereignty.
---

# Anonymous Resource Control

Sonr is pioneering a new approach to digital identity and asset management that puts users in control while preserving their privacy. By leveraging decentralized technologies like UCAN (User-Controlled Authorization Networks), IPFS (InterPlanetary File System), and DIDs (Decentralized Identifiers), Sonr enables pseudonymous access to data and resources.

### Decentralized Identifiers (DIDs)

At the core of Sonr's system are Decentralized Identifiers (DIDs). A DID is a globally unique identifier that is created and owned by the user. Unlike traditional usernames which are issued by a specific service provider, DIDs are independent and can be used across services.

Each DID has an associated DID Document which contains information about the DID, such as the public keys and service endpoints. These public keys are used to verify digital signatures, enabling authentication without revealing the user's actual identity.

### User-Controlled Authorization Networks (UCANs)

While DIDs provide a foundation for decentralized identity, UCANs enable decentralized authorization. A UCAN is essentially a token that proves the holder has been granted specific permissions by the token issuer.

In Sonr's system, users can issue UCANs to grant access to their resources stored on IPFS. For example, a user could issue a UCAN granting read-only access to a specific file to a specific DID, without revealing their own identity. The UCAN includes the necessary cryptographic proofs to verify the authorization without needing to contact the issuer.

### InterPlanetary File System (IPFS)

IPFS serves as the decentralized storage layer in Sonr's architecture. IPFS is a distributed system for storing and accessing files, websites, applications, and data. It uses content-addressing, where a file's address is a hash of its content, providing a native way to de-duplicate and verify data.

In Sonr, each user's data is stored in an IPFS node that they control. When a user wants to share data, they grant access via a UCAN rather than sending the data itself. The recipient can then retrieve the data directly from IPFS using the content address and the authorization provided by the UCAN.

### Putting it All Together

Here's a simplified example of how these pieces fit together in Sonr:

1. Alice wants to share a document with Bob, but doesn't want to reveal her identity.
2. Alice adds the document to her IPFS node, which returns a content address (hash).
3. Alice creates a UCAN granting read access to that specific content address to Bob's DID.
4. Alice sends the UCAN to Bob (e.g., via a messaging app that supports DIDs).
5. Bob's app verifies the UCAN's cryptographic proof using Alice's public DID (without needing to know Alice's real identity).
6. Bob's app retrieves the document from IPFS using the content address in the UCAN.

In this way, Sonr enables a form of anonymous resource control. Users can grant fine-grained access to their data using UCANs and DIDs, while the actual data is stored and retrieved from IPFS in a decentralized manner. This approach provides a high degree of user control and privacy, reducing dependence on centralized authorities and empowering individuals in the digital realm.
