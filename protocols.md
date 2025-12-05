## Protocols
A protocol is a system that let two parties communicate with each other.

A protocol is designed with set of properties , keeping in mind what kind of problems are we going to solve.
Ex HTTP, TCP , UDP , gRPC, FTP etc

### Properties of a protocol
- Data Format
    - Text based (XML , plain text)
    - Binary ( protobuff , RESP[redis protocol], h2, h3)
- Transfer Module
    - Message based ( UDP , HTTP)
    - Stream ( TCP , WebSockets)
-  Addressing system
    - DNS , IP , MAC , basically the source and destination identifiers
- Directionality
    - Bidirectional
    - Unidirectional
    - Full / Half duplex
- State
    - Stateless ( UDP, HTTP)
    - Stateful ( TCP, gRPC, Thrift)
- Routing
    - Proxy , Gateways
- Flow and Congestion control
- Error managment
    - Retries
    - Timeouts and Error code