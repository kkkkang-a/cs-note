# Authentications

User authentication is important since you will get the corresponding privilege after your “identity” is confirmed.

## Authentication Factors

Security research has determined that for a positive authentication, elements from at least two, and preferably all three, factors should be verified.

The three factors (classes) and some of the elements of each factor are:
- [Knowledge](multi-factor-authentications.md#knowledge): Something the user knows (password, passphrase, PINs, challenge-response, security question)
- [Possession](multi-factor-authentications.md#possession): Something the user has (ID card, security token, software token, OTP (one-time-password))
- [Inherence](multi-factor-authentications.md#inherence): Something the user is or does (fingerprint, signature, face, voice or other biometric identifiers)

### Single-Factor Authentication

As the weakest level of authentication, only a single component from one of the three categories of factors is used to authenticate an individual's identity.

This type of authentication is not recommended for financial or personally relevant transactions that warrant a higher level of security.

### Multi-Factor Authentication

[Multi-factor authentication](multi-factor-authentications.md) involves two or more authentication factors (something you know, something you have, or something you are).

Two-factor authentication is a special case of multi-factor authentication involving exactly two factors.