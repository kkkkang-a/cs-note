# Open Systems Interconnection (OSI) Model

The OSI (Open Systems Interconnection) Model is a seven-layer conceptual framework that standardizes network communication functions. Each layer is designed to perform specific tasks, ensuring smooth data transmission across diverse networks and devices.

## Layer Architecture

[Encapsulation](data-encapsulation-in-layers.md) is key to ensuring that data is correctly transmitted, routed, and delivered across a network.

- **Encapsulation**: Each layer of the sending device adds a header to the data as it passes down the stack.
- **Decapsulation**: Each layer of the receiving device removes its corresponding header as the data passes up the stack.

### Application Layer

The [application layer](application-layer-osi.md) is the topmost layer where users interact with network services. This layer facilitates communication between applications on different computers, handling services such as file transfers, email, and web browsing.

- **Examples**: Telnet, HTTP, FTP, WWW browsers
- **Responsibilities**: Providing user-level services.

### Presentation Layer

The [presentation layer](presentation-layer.md) ensures that the data sent by the application layer is readable by the receiving system. It handles data formatting, compression, and encryption to maintain the integrity of the information.

- **Examples**: JPEG, ASCII, Binary, Encryption
- **Responsibilities**: Data translation, compression, encryption.

### Session Layer

The [session layer](session-layer.md) manages and controls the dialogues (sessions) between computers. It ensures that communication sessions can be established, maintained, and terminated gracefully.

- **Examples**: NFS, SQL
- **Responsibilities**: Dialog control and synchronisation.

### Transport Layer

The [transport layer](transport-layer.md) ensures the reliable transmission of data between two hosts. It divides large data streams into smaller packets and provides error checking and flow control.

- **Examples**: TCP, UDP
- **Responsibilities**: End-to-end delivery, flow control, error correction.

### Network Layer

The [network layer](network-layer.md) is responsible for the logical addressing and routing of data, this layer ensures that packets are transmitted across different networks and arrive at their correct destination.

- **Examples**: IP, IPX
- **Responsibilities**: Packet forwarding, routing

### Data Link Layer

The [data link layer](data-link-layer.md) ensures error-free data transfer between two devices connected on the same physical medium. It breaks down packets into frames and handles issues like flow control and error detection.

- **Examples**: Ethernet, Token Ring, Frame Relay
- **Responsibilities**: Framing, physical addressing, error detection.

### Physical Layer

The [physical layer](physical-layer.md) deals with the actual hardware connections and defines the electrical and physical aspects of the data transmission process, such as cable types, signal voltages, and bit rates.

- **Examples**: RJ45, Ethernet cables
- **Responsibilities**: Transmitting bits over the physical medium.

