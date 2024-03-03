# One-Time Pad Symmetric Encryption

In cryptography, a one-time pad is a system in which a randomly generated private key is used only once to encrypt a message that is then decrypted by the receiver using a matching one-time pad and key.

Typically, a one-time pad is created by generating a string of characters or numbers that will be at least as long as the longest message that will be sent. This string of values is generated in some random fashion, such as by using a computer program with a random number generator.

Each encryption is unique and bears no relation to the next encryption, making it impossible to detect pattern.

But with a one-time pad, the decrypting party must have access to the same key used to encrypt the message; this raises the issue of how to get the key to the decrypting party safely, or how to keep both keys secure