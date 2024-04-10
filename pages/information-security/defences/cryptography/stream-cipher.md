# Stream Cipher

A stream cipher is an encryption algorithm that uses a symmetric key to encrypt and decrypt a given amount of data.

Stream ciphers generate pseudorandom bits from the key and encrypt the plaintext by XORing it with the pseudorandom bits.

It works byte by byte to transform plain text into code that's unreadable to anyone without the proper key

A symmetric cipher key, as opposed to an asymmetric cipher key, is an encryption tool that is used in both encryption and decryption.

Asymmetric keys will sometimes use one key to encrypt a message and another to decrypt the respective cipher text.

## Implementation

Stream ciphers can be implemented using algorithms that generate a key stream from a key and an initialization vector (IV). This key stream is then XORed with the plaintext stream to produce the ciphertext.

For example, given the key, the message can be encrypted and decrypted.

```
Encryption:
Original    0   0   0   1   1   1   1   1
Key (XOR)   0   1   1   0   1   1   0   0
Encrypted   0   1   1   1   0   0   1   1

Decryption:
Encrypted   0   1   1   1   0   0   1   1
Key (XOR)   0   1   1   0   1   1   0   0
Original    0   0   0   1   1   1   1   1
```

## Stream Cipher vs One Time Pad

Stream cipher:
- easy to implement
- required less key material
- less storage space, bit by bit
- depends on secrecy of key, nonce, and pseudorandom generator

One time Pad:
- theoretically unbreakable as every time a new random key stream
- long keys, more storage, very strong key distribution