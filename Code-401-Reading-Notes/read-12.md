
# Socket.IO
 ### What is the benefit of transforming data into packets?
   
Packets are intended to transfer data reliably and efficiently. Instead of transferring a large file as a single block of data, sending smaller packets helps ensure each section is transmitted successfully.

   ### UDP is often refereed to as a connectionless protocol. Why is this?
   UDP is a connectionless protocol. It is known as a datagram protocol because it is analogous to sending a letter where you don't acknowledge receipt. 
    
  No connection needs to be established between the source and destination before you transmit data.

 ### Can a socket server application have multiple socket connections?
   yes, Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to

### Can a socket connection application be connected to multiple socket servers?
   Yes, a socket connection application can connect to multiple socket

### Can an application be both a socket server and a socket connection?
   Yes, it can be applied.
<hr>

  ## Terms:
  **The observer pattern** is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.

  **Listener:**
is a function who listen to specific action to be triggered, then fire a call back function.

 **Event Handler:** is a callback routine that operates asynchronously and handles inputs received into a program (events).

**Event Driven Programming:**
Is a programming paradigm (style) in which we add events listener to specific triggers and connect them with call back functions. In which the flow of the program is determined by events such as user actions, sensor outputs, or message passing from other programs or threads.

**Event Loop:**

is like a continues loop for the event listener that keep waiting for the event to happen then fire the call back function.
is a programming construct or design pattern that waits for and dispatches events or messages in a program. The event loop works by making a request to some internal or external "event provider", then calls the relevant event handler.

 **event queue** is a repository where events from an application are held prior to being processed by a receiving program or system. Event queues are often used in the context of an enterprise messaging system.

 **call stack** is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function

**Emit/Raise/Trigger:**
Is the event starter action,  that when it happened the event will listen to it and fire a call back.
**Subscribe:**
The Publish/Subscribe pattern, also known as pub/sub, is an architectural design pattern that provides a framework for exchanging messages between publishers and subscribers. This pattern involves the publisher and the subscriber relying on a message broker that relays messages from the publisher to the subscribers. The host (publisher) publishes messages (events) to a channel that subscribers can then sign up to.

**database** is an organized collection of data, generally stored and accessed electronically from a computer system. Where databases are more complex they are often developed using formal design and modeling techniques.
<hr>

**Socket.IO** is a library that enables real-time and full-duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts; both WebSocket vs Socket.io are event-driven libraries.

Client-Side: it is the library that runs inside the browser
Server Side: It is the library for Node.js


**Why do we need Socket.IO:**
* I handle all the degradation of your technical alternatives to get full-duplex communication in real-time.
* It also handles the various support level and the inconsistencies from the browser.
* It also gives the additional feature room support for basic publish infrastructure and thinks like automatic reconnect.
* Currently, AFAIK is the most used one and easier to help with vanilla web sockets.



# WebSocket

WebSocket is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer. When clients trigger the request to the server, it does not close the connection on receiving the response; it rather persists and waits for the Client or server to terminate the request.


