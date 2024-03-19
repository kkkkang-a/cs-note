# Rainbow Table Attack

The rainbow table itself refers to a precomputed table that contains the password hash value for each plain text character used during the authentication process.

A rainbow table attack is a password cracking method that uses a special table (a “rainbow table”) to crack the password hashes in a database.

Applications don’t store passwords in plaintext, but instead encrypt passwords using [hashes](../defences/cryptography/hash-functions.md).

If hackers gain access to the list of password hashes, they can crack all passwords very quickly with a rainbow table.

## Examples

- An attacker spots a web application with outdated password hashing techniques and poor overall security. The attacker steals the password hashes and, using a rainbow table, the attacker is able to decrypt the passwords of every user of the application.
- A hacker finds a vulnerability in a company’s Active Directory and is able to gain access to the password hashes. Once they have the list of hashes they execute a rainbow table attack to decrypt the hashes into plaintext passwords.

## Defenses

The best protection against the rainbow table attack is to use a [salt](../defences/cryptography/salt.md) (random characters) in your password. i.e. instead of storing `hash(password)`, store `hash(password + salt)`, or even better `hash(salt + hash(password))`.

Since even with rainbow tables, it is going to be near impossible to store all possible salted hashes.

You have to store your salt with your hash so that you can authenticate the user.