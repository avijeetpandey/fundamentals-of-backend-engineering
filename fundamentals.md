## Request response model
The typical Backend engineering revolves heavily around request and response model , where in a client makes a request and waits for the response before moving forward.

This is how a typical request response model looks like
- The client sends the request
- Server parses the request
- Server process the request
- Server sends the response back to the client and client parses the response and then consumes it

Note - `Serialisation` and `Deserialisation` comes at the processing layer at the backend.

#### Where is request and response model used ?
The request and response model is heavily used in the following
- Web, HTTP, DNS, SSH
- RPC ( Remote procedural calls)
- SQL and DB protocols
- API ( SOAP/ REST/ GraphQL )


## Anatomy of a request and response
A request structure is defined by both client and the server

```javascript
Ex
GET / HTTP/1.1
Headers
<CRLF>
Body
```

A request has a boundary and is defined by the protocols and message format, same goes for response as well.


### Where does typical request and response model doesnot works?
It does not works on systems like
- Notification service
- Chatting application
- Very long process
- Situations in which client drops the connection


A typcial request response looks like this
> request headers -> response headers -> body/content of the page

## Sync vs Async Workload
There are two types of worloads namely `sync` and `async` one basically everything running before its done running, while the later moves on and doest not blocks the future code running when the response is ready it just resumes from that point.


### Sync I/O
- Caller sends a request and blocks everything
- Caller cannot execute the code meanwhile
- Reciever responds and the caller unblocks
- Caller and Reciever are in sync

Examples
- Programs asks os to read from the disk
    - Program main thread is taken off by the CPU
    - Read completes and program can resume the execution

### Aysnc I/O
- Caller sends a request
- Caller can work untill it gets a response
- Caller either
    - Checks if the response is ready
    - Reciver calls back when its done
    - Spins up a new thread that blocks
- Caller and reciever are in sync that is not neccesary


Note -> Synchronity is a client property