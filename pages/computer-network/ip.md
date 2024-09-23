# Internet Protocol (IP)

The Internet Protocol (IP) is a fundamental protocol used for identifying and locating devices on a network. It is responsible for the routing and delivery of data packets from one node to another across networks.

IP is a connectionless protocol, meaning it does not guarantee the delivery of data. For reliable data transmission, higher-level protocols such as TCP are used to ensure data is delivered accurately and completely.

## IP Service Model

The Internet Protocol (IP) provides a fundamental service model for delivering data across networks. It focuses on simplicity and efficiency but leaving reliability and error handling to other layers or protocols.

IP uses a unique addressing scheme to identify each device (or host) within an internetwork. Each device is assigned a unique IP address, which allows it to be located and communicated with over the network.

IP employs a datagram approach for data delivery. This means data is divided into packets (datagrams) that are sent independently through the network. Each packet may take a different route to reach its destination.

- **Connectionless Service**: IP is a connectionless protocol, meaning it does not establish or maintain a connection between the sender and receiver. Each packet is treated independently, and no prior setup is required before sending data.
- **Unreliable**: IP does not guarantee the delivery of packets. If a packet is lost, corrupted, or misdelivered, IP does not provide mechanisms to correct these issues. The network layer does its best to deliver the packet, but there are no assurances of successful delivery.
- **Best-Effort Delivery**: The IP service model operates on a best-effort basis. It attempts to deliver packets to their destination but does not provide guarantees or mechanisms for recovery in case of failure.
- **No Flow Control**: IP does not manage the flow of data between sender and receiver. There is no control over the rate at which data is sent, which means the sender may transmit data faster than the receiver can process it.
- **No Error Control**: IP does not include error control mechanisms. It does not detect or correct errors in the transmitted packets. Error checking and correction are handled by higher-layer protocols, such as TCP.

## Types of Internet Protocols

The Internet Protocol comes in two main versions.

### IPv4

[IPv4](ipv4.md) (Internet Protocol version 4) is the fourth version of IP and uses a 32-bit address scheme. An IPv4 address is expressed as four decimal numbers separated by dots, each ranging from 0 to 255. IPv4 addresses can be assigned either manually or through DHCP (Dynamic Host Configuration Protocol). While widely used, IPv4 lacks advanced security features such as built-in authentication and encryption.

IPv4 is organised into five classes:

- **Class A**: Supports large networks with many hosts (e.g., 10.0.0.0 to 10.255.255.255).
- **Class B**: Suitable for medium-sized networks (e.g., 172.16.0.0 to 172.31.255.255).
- **Class C**: Designed for small networks (e.g., 192.168.0.0 to 192.168.255.255).
- **Class D**: Used for multicast groups (e.g., 224.0.0.0 to 239.255.255.255).
- **Class E**: Reserved for experimental purposes (e.g., 240.0.0.0 to 255.255.255.255).

### IPv6

[IPv6](ipv6.md) (Internet Protocol version 6) is the most recent version of IP and provides a 128-bit address scheme. An IPv6 address consists of eight groups of four hexadecimal digits separated by colons. IPv6 offers a significantly larger address space compared to IPv4, addressing the limitations of IPv4’s address exhaustion.

IPv6 includes enhanced security features such as:

- **Authentication**: Ensuring data integrity and verification of sender identity.
- **Encryption**: Protecting data from unauthorized access.

IPv6 supports end-to-end connection integrity and simplifies network configuration through features like automatic address assignment. Its larger address space facilitates the expansion of the internet and supports a vast number of devices and services.
