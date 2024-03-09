# Passkey Credentials

> WebAuthn and Passkeys are complementary technologies that work together to create a passwordless login experience for the user. They both leverage public key cryptography for secure authentication and are designed to be resistant to phishing.

WebAuthn, or Web Authentication API, is a specification of a JavaScript API that allows applications to communicate with authenticators such as key fobs or fingerprint readers. It is a part of the FIDO2 set of standards, which aim to increase security and prevent phishing attacks[1](https://curity.io/resources/learn/webauthn-overview/). WebAuthn is a core component of the FIDO2 Project, published by the World Wide Web Consortium (W3C) and the FIDO Alliance[3](https://teampassword.com/blog/passkey-vs-webauthn).

Passkeys, on the other hand, are a type of authentication method that allows users to access online services without using passwords. They use asymmetric public key cryptography for secure authentication[3](https://teampassword.com/blog/passkey-vs-webauthn). Passkeys are built on the WebAuthn standard and are designed to be resistant to phishing, always strong, and have no shared secrets[6](https://support.apple.com/en-us/102195).

# **How WebAuthn Works**

WebAuthn works by enabling the creation and use of origin-scoped, public-key credentials to authenticate users. It supports the use of BLE, NFC, and USB-roaming U2F or FIDO2 authenticators, as well as platform authenticators which let users authenticate with their fingerprints or screen locks[2](https://developers.google.com/codelabs/webauthn-reauth). WebAuthn has three main entities: the authenticator, the client, and the relying party. The authenticator is the device that generates the public-private key pair and signs the authentication assertion. The client is the user's device that interacts with the authenticator and the relying party. The relying party is the server that verifies the authentication assertion[7](https://webauthn.me/introduction).

# **How Passkeys Work**

Passkeys are built on the WebAuthn standard and use public key cryptography. During account registration, the operating system creates a unique cryptographic key pair to associate with an account for the user. One of these keys is public and is stored on the server, while the other key is private and is kept secure on the user's device[6](https://support.apple.com/en-us/102195).

# **Implementation**

To implement WebAuthn, you need to act as a WebAuthn Relying Party. The Relying Party code will be split between the server-side and the client-side. The server-side code is responsible for generating the options for WebAuthn ceremonies, validating responses, and storing passkeys. The client-side code, primarily JavaScript, is responsible for communicating with the server, invoking the WebAuthn API, and translating between message formats required for each[5](https://webauthn.wtf/develop/build-it-yourself).

# **Security**

WebAuthn uses public key cryptography, which means the user's private key never leaves their device, making it resistant to phishing attacks. It leverages industry-standard cryptographic algorithms and protocols to ensure the highest level of security. It utilizes authenticators to confirm the user's identity and create highly secure public-private key pairs[10](https://auth0.com/blog/webauthn-a-short-introduction/).

Passkeys, being built on the WebAuthn standard, also use public key cryptography for secure authentication. They are designed to be resistant to phishing and are always strong. They are designed so that there are no shared secrets, which further enhances their security[6](https://support.apple.com/en-us/102195).

However, it's important to note that while WebAuthn and Passkeys are phishing-resistant, they are not immune to all types of attacks. Therefore, proper implementation and security best practices on both the client and server sides are crucial to maximizing their security benefits[10](https://auth0.com/blog/webauthn-a-short-introduction/).
