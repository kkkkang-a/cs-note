# Data Link Layer

Data link layer transmits data between different devices in the same network (LAN) based on their MAC addresses.

- **Framing the Data Bits**: Divides the stream of bits received from the network layer into manageable frames.
- **Moving Frames**: Transfers frames from one hop (node) to the next in the network.
- **Physical Addressing**: Provides physical addresses (MAC addresses) for identifying the sender and receiver.
- **Flow Control**: Prevents the sender from overwhelming the receiver with too mushy data too quickly.
- **Error Control**: Adds reliability by detecting and correcting errors in the data transmitted over the physical layer. It checks any error in the MAC address of the source and the destination.
- **Access Control**: Manages which device has control over the network link at any given time to avoid conflicts.

Data link layer only checks the error between nodes (the delivery address). Transport layer checks the actual content in the message, such as sequencing and reassembly.