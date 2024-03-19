# Asymmetric-Key Cryptography

Each key pair consists of a public key and a corresponding private key.

Key pairs are generated with cryptographic algorithms based on mathematical problems termed one-way functions.

In a asymmetric encryption system, anyone with a public key can encrypt a message, yielding a cipher text, but only those who know the corresponding private key can decrypt the cipher text to obtain the original message.

## Diffie-Hellman Key Exchange

Diffie–Hellman key exchange is a mathematical method of securely exchanging cryptographic keys over a public channel and was one of the first public-key protocols.

## Digital Signature

A [digital signature](digital-signatures.md) gives the receiver reasons to believe the message was created and sent by the claimed sender.

It also ensures non-repudiation which prevents the sender from later claiming that they didn't send a message or they didn't participate in a transaction.

## Certification Authorities

Certificate Authorities (CAs) are trusted third-party entities responsible for issuing digital certificates, which are used to establish trust in the identities of entities on the internet, such as websites, servers, and individuals.

- **Certificate Issuance**: When an entity (such as a website) requests a digital certificate, they submit a Certificate Signing Request (CSR) to the CA. The CSR includes the entity's public key and identifying information.
- **Identity Verification**: The CA verifies the identity of the entity by validating the information provided in the CSR. This process may involve verifying domain ownership, legal registration, or other forms of identity verification.
- **Certificate Signing**: Once the identity is verified, the CA digitally signs the entity's certificate using its private key. This signature ensures the integrity and authenticity of the certificate.
- **Certificate Distribution**: The CA issues the signed certificate to the entity, who can then install it on their server or use it for other purposes, such as code signing or email encryption.
- **Certificate Revocation**: CAs maintain Certificate Revocation Lists (CRLs) or use Online Certificate Status Protocol (OCSP) to revoke certificates if they are compromised or no longer valid (Out of Scope).