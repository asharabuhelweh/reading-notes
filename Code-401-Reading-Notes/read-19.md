# AWS: Events


## Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server
- In Express server we can connect and send HTTP requests to a specific endpoints and connect them with handler functions on the same server
 - Using AWS we can separate the routing process and the function handler, where you send the HTTP request using AWS API Gateway and integrate them with Lambda functions.

## List the AWS Database offerings and talk about the pros and cons of each
AWS Dynamo :is a No-SQL database allow you to store data and manipulate it, also it has a package called Dynamoose will allow you to connect with DynamoDB more easily.

AWS S3 :Simple Storage service, allow you to store specific issues or maybe back-up your data for later time. 

### What’s the difference between a FIFO and a standard queue?
- Standard queues guarantee that a message is delivered at least once and duplicates can be introduced into the queue. 
- FIFO queues ensure a message is delivered exactly once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue.


### How can the server be assured a message was properly received?
By adding to the server Messaging Queue 


## Term

### Serverless API
 Its is an API deployed by serverless service. server is not locally in our app.

### Triggers
A trigger is a Lambda resource or a resource in another service that you configure to invoke your function in response to lifecycle events, external requests, or on a schedule. Your function can have multiple triggers. Each trigger acts as a client invoking your function independently.
### Dynamo vs Mongo

- MongoDB Open Source, and can be deployed anywhere. DynamoDB is only available on AWS.
- DynamoDB is a fully managed AWS service, MongoDB can be self installed or fully managed with MongoDB Atlas.
- DynamoDB as an integrated AWS service makes it easier to develop end to end solutions.
- DynamoDB uses tables, items and attributes, MongoDB uses JSON-like documents.
- DynamoDB supports limited data types and smaller item sizes; MongoDB supports more data types and has fewer size restrictions.

### Dynamoose vs Mongoose

Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment. Mongoose supports both promises and callbacks.
Packages to connect to MongoDB and DynamoDB and manipulate the data more easily.



## SQS and SNS

### SQS (Simple Queue Service)

  It's a Distributed queuing system.
- Messages are not pushed to receivers, receivers have to poll SQS to receive messages
- Messages can’t be received by multiple receivers at the same time
- Anyone's receiver can receive a message, process and delete it, other receivers do not receive the same message later
- Mainly used to decouple applications or integrate applications
- Messages can be stored in SQS for a short duration of time (max 14 days)

### SNS (Simple Notification Service)

- Fast, flexible, and fully managed push notification service that lets you send individual messages or bulk messages
- Distributed publish/subscribe system
- Messages are pushed to subscribers as and when they are sent by publishers to SNS
- SNS supports several end points such as email, SMS, HTTP endpoint, and SQS
- If you want an unknown number and type of subscribers to receive messages, you need SNS
  

## Key Differences

### Entity Type

SQS : Queue (similar to JMS, MSMQ).
SNS : Topic-Subscriber (Pub/Sub system).

### Message consumption

SQS : Pull Mechanism — Consumers poll messages from SQS.
SNS : Push Mechanism — SNS pushes messages to consumers.

### Persistence

SQS : Messages are persisted for some duration is no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days.

SNS : No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.
In SQS the message delivery is guaranteed but in SNS it is not.

### Consumer Type

SQS : All the consumers are supposed to be identical and hence process the messages in exact same way.

SNS : All the consumers are (supposed to be) processing the messages in different ways.

### Use Cases

#### Choose SNS if

* You would like to be able to publish and consume batches of messages.
* You would like to allow same message to be processed in multiple ways.
* Multiple subscribers are needed.

#### Choose SQS if

* You need a simple queue with no particular additional requirements.
* Decoupling two applications and allowing parallel asynchronous processing.
* Only one subscriber is needed.
* We can design fanout pattern by using both SNS and SQS. In this pattern, a message published to an SNS topic is distributed to multiple SQS queues in parallel.

