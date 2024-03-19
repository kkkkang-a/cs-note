# Dictionary Attack

A dictionary attack is a systematic method of guessing a password by trying many common words and their simple variations, or sometimes trying thousands or millions of likely possibilities often obtained from lists of past security breaches.

The attacker attempts to guess a password by systematically trying out every possible word in a dictionary.

A dictionary attack is considered a type of [brute-force attack](brute-force-attack.md). In common use though a brute-force attack will use a systematic approach to try all possible passwords. 

The dictionary attack is fast, but limited by the word in the dictionary. It is usually limited to passwords of a reasonable length.

It is possible to achieve a time–space tradeoff by pre-computing a list of hashes of dictionary words and storing these in a database using the [hash](../defences/cryptography/hash-functions.md) as the key. A more refined approach involves the use of [rainbow tables](rainbow-table-attack.md).