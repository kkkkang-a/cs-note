# Symmetric-Key Cryptography

Symmetric-key cryptography is the encryption methods in which both the sender and receiver share the same key.

Symmetric key ciphers are implemented as either block ciphers or stream ciphers.

A block cipher enciphers input in blocks of plaintext as opposed to individual characters, the input form used by a stream cipher.

## Block Cipher

Block ciphers are cryptographic algorithms that operate on fixed-length groups of bits, called blocks.

These ciphers take a block of plaintext bits and a key as inputs and output a block of ciphertext bits of the same size.

The key is used to determine the mapping between plaintext and ciphertext.

Popular block ciphers include:
- Data Encryption Standard (DES)
- Advanced Encryption Standard (AES)
- Triple DES (3DES)
- Blowfish


## Stream Cipher

A stream cipher is an encryption algorithm that uses a symmetric key to encrypt and decrypt a given amount of data.

It can be viewed as approximating the action of a proven unbreakable cipher, the [one-time pad](./one-time-pad.md) (OTP).

A symmetric cipher key, as opposed to an asymmetric cipher key, is an encryption tool that is used in both encryption and decryption.

Asymmetric keys will sometimes use one key to encrypt a message and another to decrypt the respective ciphertext.

Examples of stream ciphers include:
- A4 for GSM cellular networks
- RC4 algorithm for for wireless networks
- Salsa20/ChaCha20 family of algorithms

### Inplementation

Stream ciphers can be implemented using algorithms that generate a keystream from a key and an initialization vector (IV). This keystream is then XORed with the plaintext stream to produce the ciphertext.

### Stream Cipher vs One Time Pad

Stream cipher:
- easy to implement
- required less key material
- less storage space, bit by bit
- depends on secrecy of key, nonce, and pseudorandom generator

One time Pad:
- theoretically unbreakable as every time a new random keystream
- long keys, more storage, very strong key distribution