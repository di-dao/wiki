# Cryptographic System

# Digital Signatures

The following algorithms and systems are used to provide authenticity over data received on the Sonr Network. The default protocol for user facing signature actions is Multi-Party computation. DKLS (2-Party) MPC protocol is a secure and efficient method for two parties to perform joint computations within a multi-party setting, with a particular focus on threshold ECDSA signatures. Its use of OT and OT Extension makes it a practical choice for real-world applications where secure, distributed computation is required.

## DKLSv1 (2-Party)

DKLS (2-Party) Multi-Party Computation (MPC) refers to a cryptographic protocol designed for secure computation between two parties within a larger multi-party setting. The DKLS protocol, named after its authors Doerner, Kondi, Lee, and Shelat, is particularly focused on threshold ECDSA (Elliptic Curve Digital Signature Algorithm), which is a digital signature scheme that is widely used for securing transactions in blockchain and other cryptographic applications.

The DKLS protocol enables two parties to jointly compute a function over their private inputs without revealing those inputs to each other. This is particularly useful in scenarios where trust is distributed, such as in decentralized financial systems. The protocol is based on Oblivious Transfer (OT) and uses an optimized multiplication algorithm known as OT-MUL, which is a secure multiplication protocol derived from Gilboa's OT-based secure multiplication protocol \[Gil99]. This approach is hardened and combined with OT Extension, a technique that reduces the number of OTs required, thereby speeding up the computation and reducing the overall cost to a few thousand hashes, which is only a few milliseconds on modern hardware[3](https://research.nccgroup.com/2023/08/25/real-world-cryptography-conference-2023-part-ii/)[5](https://www.silencelaboratories.com/blog-posts/a-compute-perspective-of-mpc-tss-paillier-in-ecdsa-revisited-2).

The DKLS 2-party multiplication algorithm is a fundamental building block in MPC and is designed to be efficient and secure. It includes simple consistency checks that eliminate the need for expensive zero-knowledge proofs while maintaining a high level of security. This makes the DKLS protocol suitable for practical deployment, even in user-facing applications running on commercial off-the-shelf devices[3](https://research.nccgroup.com/2023/08/25/real-world-cryptography-conference-2023-part-ii/)[5](https://www.silencelaboratories.com/blog-posts/a-compute-perspective-of-mpc-tss-paillier-in-ecdsa-revisited-2).

***

# Data Privacy

All resources in the Sonr network are encrypted and backed up to IPFS with a matching user IPNS record by default. The network then employs a decryption method when user sessions are active in order to provide authorized access to end-data.

Zero-knowledge accumulators are cryptographic primitives that allow one to represent a set of elements in a compact form while enabling the proof of membership or non-membership of an element in the set without revealing any additional information about the set. They are an extension of cryptographic accumulators with the additional property of zero-knowledge.

### **Cryptographic Accumulators**

A cryptographic accumulator is a data structure that compresses a set of values into a single short representation. This representation, or accumulator value, allows the generation of a membership proof, also known as a witness, which is a small piece of data that proves whether a particular value is part of the set[6](https://asecuritysite.com/zero/witness).

### **Zero-Knowledge Property**

The zero-knowledge property of an accumulator ensures that the accumulator value and the witness do not leak any information about the elements in the set. This property is crucial for privacy-preserving applications, as it allows one to prove set membership without revealing the set's contents or any specific element within it[1](https://par.nsf.gov/servlets/purl/10043866)[3](https://www.sciencedirect.com/science/article/abs/pii/S2214212619302698).

### **Witnesses in Zero-Knowledge Proofs**

In the context of zero-knowledge proofs, a witness is a piece of information that allows one to efficiently verify a statement. For example, if the statement is that a number is a square modulo an RSA modulus, a witness would be an integer that, when squared, equals the given number modulo the modulus[2](https://crypto.stackexchange.com/questions/43462/what-is-a-witness-in-zero-knowledge-proof).

### **Zero-Knowledge Accumulator Constructions**

The first construction of a zero-knowledge dynamic universal accumulator was proposed to be perfect zero-knowledge and secure under the q-SBDH assumption. This construction allows for the dynamic addition of elements to the set and the generation of witnesses without compromising the privacy or soundness of the system[1](https://par.nsf.gov/servlets/purl/10043866).

### **Practical Implementations**

Recent advancements have focused on improving the practicality of zero-knowledge accumulators. For instance, Curve Trees are a transparent and efficient construction for zero-knowledge accumulators that do not require a trusted setup. They are based on commit-and-prove techniques and can generate small proof sizes for large sets[4](https://eprint.iacr.org/2022/756).

### **Applications**

Zero-knowledge accumulators are used in various privacy-aware applications, such as anonymous payments, credentials, and whitelists. They enable users to prove knowledge of an element in a large set without revealing the element itself or any other elements in the set[4](https://eprint.iacr.org/2022/756).

### **Security Properties**

Good zero-knowledge accumulators should satisfy three main properties:

* **Completeness**: The verifier should accept a valid proof with high probability.

* **Soundness**: It should be nearly impossible for a dishonest prover to convince the verifier of a false statement.

* **Zero-Knowledge**: The proof should not leak any information about the witness or the set beyond the fact that the statement is true[5](https://en.wikipedia.org/wiki/Zero-knowledge_proof)[11](https://www.linkedin.com/pulse/zero-knowledge-proof-enhancing-privacy-security-digital-amit-chandra).

***

# Encryption Schemes

The following encryption schemes have been tested or currently employed by the Sonr architecture.

* Public key encryption key exchange: ECDH (P256), ECDH (P384), ECDH (P521), X25519 and X448.

* Public key encryption: RSA and ECIES.

* Hashing method for key derivation (HKDF): SHA256, SHA384 and SHA512.

* Symmetric key: 128-bit AES GCM and 256-bit AES GCM.

All of the above methods are compatible with most systems. For this, Bob and Alice could pick an elliptic curve to define their key pair, and then use a given hashing methods to derive an encryption key. This is normally achieved with HKDF (HMAC Key Derivation Function).

## DAED

AEAD encryption functions allow you to create keysets that contain keys for encryption and decryption, use these keys to encrypt and decrypt individual values in a table, and rotate keys within a keyset.

## ECIES

With ECC (Elliptic Curve Cryptography), we have an opportunity to use both the power of public-key encryption, with the speed and security of symmetric key encryption.

## Fully Homomorphic Encryption

Fully Homomorphic Encryption (FHE) is a sophisticated encryption scheme that allows computations to be performed on encrypted data, producing an encrypted result that, when decrypted, matches the result of operations performed on the plaintext. This means that data can be processed without ever exposing its contents, ensuring privacy and security even in untrusted environments.

