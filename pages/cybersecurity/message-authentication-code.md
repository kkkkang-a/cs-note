# Message Authentication Code

A Message Authentication Code (MAC) is a string of bits that is sent alongside a message. The MAC depends on the message itself and a secret key. No one should be able to compute a MAC without knowing the key. 

It is similar to a [hash](hash-functions.md), except that it is based on a secret key.

Unlike hash functions, MAC guarantees the integrity and authentication of sender.

## Features

Any alteration in the message or the key generates a distinct MAC. Without the secret key, attackers can't determine or validate the MAC.

Similar to the hash function, receivers compute their own MAC using the shared key and compare it with the received MAC to verify integrity.

When secret key information is included with the data that is processed by a cryptographic hash function, the resulting hash is known as an HMAC.

HMAC is a recipe for turning hash functions (such as MD5 or SHA256) into MACs.

The authenticity of the message can be determined by using the same secret key to decrypt the MAC to compare the HMAC value.