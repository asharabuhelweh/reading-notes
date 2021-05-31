# Message Queues

## Review
## What does it mean that web sockets are bidirectional? Why is this useful?

 WebSockets allow for full-duplex bidirectional communication. This enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time.

## Does socket.io use HTTP? Why?

Yes, it needs an HTTP connection to allows the first handshake in the open-system connection. It requires an HTTP server for the initial upgrade handshake. So even if you don't supply Socket.io with an HTTP server, it will create one for you.

## What happens when a client emits an event?

server side will  listen to that event and then handle the data received form the client by call back function.

## What happens when a server emits an event?

Some other event listeners will be listening to that event. If the event was emitted, it would call the event handler

## What happens if a client “misses” an event?

 no listening to that event 
## Terms

* Socket: it is a general term that refers to a data or power port that allows other data tracks to reach for and cause changes. In the web world, the socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to.
* Web Socket: is a computer communications protocol providing full-duplex communication channels over a single TCP connection.
* Socket.io: it is a package that allows us to use Websockets and other features when we build web applications. It enables real-time, bidirectional, and event-based communication.
* Client: it could be a browser (front-end) or a server with an open socket to the original server.
* Server: The computer contains the software that opens the serving socket to the client.
* OSI Model: stands for Open-System Integration model, is a model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.
* TCP Model: Transmission Control Protocol is the conceptual model and communications protocols used in the Internet and similar computer networks.
* TCP is a standard that defines establishing and maintaining a network conversation through which application programs can exchange data.
* UDP: User Datagram Protocol is a communications protocol primarily used to establish low-latency and loss-tolerating connections between applications on the internet. It is generally faster than TCP because it does not perform feedback checking on data received by the client.
* Packets: it is a form of data that consists of a small amount of information with a port number, IP addresses to the sender and the caller, and a tail part that contains some protocol information.


**A message queue** is a form of asynchronous service-to-service communication used in serverless and microservices architectures.

* Messages are stored on the queue until they are processed and deleted.

* Each message is processed only once, by a single consumer.

* Message queues can be used to decouple heavyweight processing, to buffer or batch work, and to smooth spiky workloads.

## Rooms

A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

![pic](https://socket.io/images/rooms.png)

**Default room**
Each Socket in Socket.IO is identified by a random, unguessable, unique identifier Socket#id. For your convenience, each socket automatically joins a room identified by its own id.

**With multiple Socket.IO servers**
ike global broadcasting, broadcasting to rooms also works with multiple Socket.IO servers.

You just need to replace the default Adapter by the Redis Adapter

![](https://socket.io/images/rooms-redis.png)

## Room events
* create-room (argument: room)
* delete-room (argument: room)
* join-room (argument: room, id)
* leave-room (argument: room, id)