# Information Security

Information security refers to the protection of your system and data from unauthorised access, modification, or disclosure.

## Categories

Security aspects:
- [Computer Security](categories/computer-security.md)
- [Network Security](categories/network-security.md)

Defences and threats:
- [Threats](threats/threats.md)
- [Defences](defences/defences.md)

## Security Triad (CIA Triad)

### Confidentiality

Confidentiality measures are designed to prevent sensitive information from unauthorised access attempts. The information is access only by authorised individuals or entities.

Confidentiality can be achieved through encryption, access controls, authentication mechanisms, and data classification.

### Integrity

The consistency, accuracy and trustworthiness of data must be maintained over its entire lifecycle. Data must not be changed in transit, and steps must be taken to ensure it can't be altered by unauthorised entities.

Integrity mechanisms such as [hash functions](defences/cryptography/hash-functions.md), [digital signatures](defences/cryptography/digital-signatures.md), and access controls help verify the authenticity and reliability of data.

### Availability

Information should be consistently and readily accessible for authorised parties. This involves maintaining hardware and technical infrastructure and systems that hold and display the information.

Measures such as redundancy, backups, disaster recovery plans, and resilient network architectures are employed to maintain availability and mitigate the impact of attacks or system failures.