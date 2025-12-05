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

## OSI Model
OSI stands for Open systems interconnection model , but before we discuss the OSI model lets understand why we need the model in the first place.

#### Why a communication model is required ?
- Agnostic applications
    - Without a standard model, the application must have knowledge of underlying medium, imagine you are publishing an app and it should work with all of wifi or fiber or LTE having different modes of communication will lead to chaos
- Network equipment management
    - It becomes easy to upgrade as all will follow the same communication model
- Decoupled innovation
    - Innovation can be done seperately at each level without affecting the other models.

### Layers of OSI model
There are 7 layers in OSI model and they are
- Layer 7 => Application ( HTTP/FTP/gRPC)
- Layer 6 => Presentation ( encoding, serialisation)
- Layer 5 => Session ( connection establishment, TLS)
- Layer 4 => Transport ( UDP / TCP)
- Layer 3 => Network ( IP )
- Layer 2 => Data link ( Frames, Mac address)
- Layer 1 => Physical (electrical signal or waves)