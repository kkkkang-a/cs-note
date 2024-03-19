# Digital Signature

A digital signature is a cryptographic technique used to provide authenticity, integrity, and non-repudiation to digital messages or documents.

It serves as the digital equivalent of a handwritten signature or a stamped seal on a paper document.

It takes the following process:

1. **Key Generation**: The signer generates a pair of cryptographic keys—a private key and a corresponding public key. The private key is kept secret and known only to the signer, while the public key is freely distributed.
2. **Signing**: To sign a message or document, the signer uses their private key to perform a cryptographic operation on the message, creating a unique digital signature.
3. **Verification**: The recipient of the signed message or document uses the signer's public key to verify the digital signature. If the signature is valid, it confirms the authenticity and integrity of the content, as well as the signer's identity.