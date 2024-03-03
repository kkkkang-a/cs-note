# Hash Functions

A hash function is a mathematical algorithm that takes an input and produces a fixed-size string of characters, which is typically a hexadecimal number.

The output, often called a hash value or hash code, is unique to the input data.

## Applications

- **Message Integrity**: Hash functions are commonly used to ensure the integrity of messages or data. A short "digest" of the files is generated using a hash function and stored alongside the message. When retrieving the message, the digest is recomputed, and if it matches the stored value, it verifies the integrity of the message. This is crucial in data transmission and storage to detect any tampering or corruption.
  
- **Password Login**: In systems requiring password authentication, storing passwords in plaintext is a significant security risk. Hash functions provide a solution by securely hashing passwords before storing them. During login attempts, the entered password is hashed and compared to the stored hash, preventing exposure of the actual password even if the database is compromised.

## Properties

### One-Wayness

Encryption is a two-way function; hashing is a one-way function.

While it's technically possible to reverse-hash something, the computing power required makes it unfeasible. Hashing is one-way.

One-wayness implies that given the output (hash), it's computationally infeasible to determine the original input. This property is vital in password storage, where even if an attacker obtains the hash, it's challenging to reverse-engineer the password.

### Collision Resistance

Collision resistance refers to the property of a hash function where it's extremely difficult to find two different inputs that produce the same hash output.

In simpler terms, an attacker cannot find two files or inputs (x and y) such that the hash results for both x and y are the same. This property ensures the uniqueness of hash values, critical in applications where data integrity is paramount, such as digital signatures and data verification.

### Second Preimage

Second preimage resistance is an expected property of cryptographic hash functions whereby it is computationally infeasible to find a second input that produces the same hash output as a given known input.

In other words, given a hash function and one document (or one hash), it's challenging for an attacker to find another document that results in the same hash. A successful second preimage attack would have significant implications for security, as it could lead to the creation of fraudulent data or the compromise of authentication systems.

If a second preimage attack were practical against the cryptographic hash functions that we deploy, it would undermine the trust and reliability of various security protocols and mechanisms reliant on hash functions. Thus, ensuring the robustness of hash functions against such attacks is crucial for maintaining the integrity and security of cryptographic systems.