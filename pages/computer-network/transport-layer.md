# Transport Layer

- **Moving Messages**: Delivers message from one process to another.
- **Port Addressing**: As many processes may be running on the same communicating hosts, it is necessary to identify the desired process out of many processes. For this, the transport layer header must include a service port address in each segment (e.g. HTTP: port 80; SMTP: port 25)
- **Segmentation and Reassembly**: A message is divided into segments by the transport layer with each segment being given a sequence number. This sequence numbers enable te destination transport layer to reassemble the segments in exact order as they were sent by the sender.
- **Flow Control**: 
- **Error Control**: The transport layer provides process-to-process error control. It checks not the address (this is checked in the data link layer).

  

Transport layer protocol proceeds logical communication between hosts. Deliver the message after receiving the message to the actual running process.