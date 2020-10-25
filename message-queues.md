# Message Queues

**Message queuing:** allows applications to communicate by sending messages to each other. The message queue provides temporary message storage when the destination program is busy or not connected.

**Message queue** provides an asynchronous communications protocol, which is a system that puts a message onto a message queue and does not require an immediate response to continuing processing

**Message:** the message is the data transported between the sender and the receiver application;it's essentially a byte array with some headers at the top.

**the queue:** is a line of things waiting to be handled,starting at the beginning of the line and processing it in sequential order.

**event:** is What event has happened during transporting data (delete, add, update or connection lost ...etc)

**The payload :** is the data associated with the event.

**Namespace:** It is a declarative region that provides a scope to the identifiers (the names of types, functions, variables, etc) inside it.

- Namespaces are used to organize code into logical groups and to prevent name collisions that can occur especially when your codebase includes multiple libraries.

- **Default namespace** We call the default namespace / and it’s the one Socket.IO clients connect to by default, and the one the server listens to by default.

***

1. What does it mean that web sockets are bidirectional? Why is this useful?
Web sockets are bidirectional because you can push information both ways, from client to server and from server to client.

2. Does socket.io use HTTP? Why?
Socket.io does use HTTP to make the initial connection even when websockets can be used

3. What happens when a client emits an event?
When a client emits an event, the server is listening for it and then handles it however it has been told to.

4. What happens when a server emits an event?
When a server emits an event, it is emitted to wherever it's been told. It goes back to a client that's listneing for it, accepts the payload and then goes on with its business.

5. What happens if a client “misses” an event?
There isn't any error handling when using sockets.io, so it's a best-efforts process. Unhandled events are just ignored.

6. How can we mitigate this?
We can use a queue! We can keep the messages in a structure (maybe just an object) that we treat as a queue and each time one is received we'll delete it from the queue, but we can also have a listener to get all messages not received while offline. Cool!

## Common Terminology

|    **Term**    | **Definition**  |
| -------------- | ----------- |
| Web Socket | technology that makes it possible to open a two-way interacive communication session between clients and server  |
| Socket.io | real time, bidirectional event-based communication library    |
| Client | Connected and communicating through server    |
| Server | Connection hub in socket.io, enabling communication between itself and clients |