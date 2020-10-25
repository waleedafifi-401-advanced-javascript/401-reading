![](https://miro.medium.com/max/811/1*tOitxCwTNcS3ESstLylmtg.png)


## Web Sockets
- A communication Protocol which provides bidirectional communication between the Client and the Server over a TCP connection, WebSocket remains open all the time so they allow the real-time data transfer. When clients trigger the request to the Server it does not close the connection on receiving the response, it rather persists and waits for Client or server to terminate the request.

## Socket.io
- It is a library which enables real-time and full duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts, each of which use WebSockets, but also provide additional functionality such as broadcasting, namespacing, and other means of segmenting connected clients into groups.

  - Client Side: it is the library that runs inside the browser
  - Server Side: It is the library for Node.js

## Connections
- With TCP, you connect directly to a server with a keep-alive type of connection.
- With Socket.io, you connect to a server over HTTP. The session is “kept alive” through it’s internal use of the WebSocket Protocol, with session information being preserved.

![](https://socket.io/images/rooms.png)

__What is the benefit of transforming data into packets?__  
This is an efficient way of transfering data over networks and it limits latency.  

__UDP is often refereed to as a connectionless protocol. Why is this?__  
This is because with UPD no connection needs to be established between the origin and destination before tranferring data.  

__Can a socket server application have multiple socket connections?__  
Yes, a socket server can have more than one socket connection. We did this during our lab.  

__Can a socket connection application be connected to multiple socket servers?__  
I do not believe so. Each socket is bound to a single port.  

__Can an application be both a socket server and a socket connection?__   
It seems that a socket is mostly used to connect to a socket server, and not to be a server itself. However, I don't see why you could not have both in the same application.  



|Term | Definition |  
|---|---|
| OSI Model | OSI stands for Open System Interconnection. It is a conceptual framework for understanding the networking process. The seven layers of OSI are Physical, Data Link, Network, Transport, Session, Presentation, and Application.|
| TCP Model | This is a more concise version of the OSI Model, and it consists of four layers: Application, Transport, Internet, and Network.|
|TCP | This stands for Transmission Control Protocol. In this, the server must be listening for connections from clients.|
|UDP | This stands for User Datagram Protocol. Unlike TCP, there is no need to establish a connection before transfering data.|
| Packets | A unit of data that goes from one place to another over a network.|
| Socket | A socket is an endpoint for sending and receiving data. Sometimes this refers to an internet socket, where a socket is identified to other hosts by its socket address.|
