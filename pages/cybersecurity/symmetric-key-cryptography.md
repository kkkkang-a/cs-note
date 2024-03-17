# Symmetric-Key Cryptography

Symmetric-key cryptography is the encryption methods in which both the sender and receiver share the same key.

Symmetric key ciphers are implemented as either block ciphers or stream ciphers.

A block cipher enciphers input in blocks of plaintext as opposed to individual characters, the input form used by a stream cipher.

## Block Cipher

A [block cipher](pages/cybersecurity/blocker-cipher.md) breaks down plaintext messages into fixed-size blocks before converting them into ciphertext using a key.

Popular block ciphers include:
- Data Encryption Standard (DES)
- Advanced Encryption Standard (AES)
- Triple DES (3DES)
- Blowfish

## Stream Cipher

A [stream cipher](pages/cybersecurity/stream-cipher.md) breaks a plaintext message down into single bits, which then are converted individually into ciphertext using key bits.

It can be viewed as approximating the action of a proven unbreakable cipher, the [one-time pad](pages/cybersecurity/one-time-pad.md).

Examples of stream ciphers include:
- A4 for GSM cellular networks
- RC4 algorithm for for wireless networks
- Salsa20/ChaCha20 family of algorithms