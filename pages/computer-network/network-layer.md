# Network Layer

The network layer links different networks (WAN) based on their IP addresses and is responsible for delivering individual packets from the source host to the destination host.

Network layer has following key responsibilities:

- **Moving Packets**: The network layer is responsible for delivering individual packets from the source host to the destination host.
- **Logical Addressing**: This layer uses logical addresses to differentiate between source and destination systems. It adds a header to each packet containing the sender’s and receiver’s addresses.
- **Routing**: In large networks formed by connecting multiple independent networks or links, the network layer handles the routing of packets to exude they reach their final destination.

## Data Transfer

The network layer at source, destination and routers are responsible for host-to-host delivery and for routing the packets through the routers or switches.

>[!NOTE]
> Using the [data link layer](data-link-layer.md) is not sufficient to transfer a packet across different networks. The data link layer only contains information necessary for communication within a local network (LAN). It uses [MAC addresses](mac-addresses.md) to identify devices on the same network but cannot handle communication across networks with different IP addresses.
> 
> This is where the network layer comes in. It facilitates communication across networks, using [IP addresses](ip-addresses.md) to route packets from one network to another.
> 
> While the data link layer focuses on the physical transmission of data, the network layer ensures the logical addressing and routing necessary for data to travel across multiple networks, such as from one WAN to another.

## Protocols

- [Internet Protocol (IP)](ip.md)
- [Address Resolution Protocol](arp.md)

## Network Address Translation