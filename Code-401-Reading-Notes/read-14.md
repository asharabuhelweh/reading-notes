
# Event Driven Architecture

### What’s the difference between a FIFO and a standard queue?

FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.

### How can the server be assured a message was properly received?

On the client side simply emit the event with your data, the function will be called whenever the server responds to the event
and On the server side get called with the data and the callback handle to send the response


### What classic design pattern is best represented by event driven programming?

The Observer Design Pattern

## How do you test an event driven system?

Using jest we can mock some event emits and test against event handlers. If we receive an acknowledgement from the client, the test will pass, otherwise it needs fixes.

## Terms

### FIFO Queue

A FIFO queue is a queue that operates on a first-in, first-out (FIFO) principle. This means that the request (like a customer in a store or a print job sent to a printer) is processed in the order in which it arrives. ... In queuing theory, the rule governing queue operation is known as queuing discipline.

### Pub/Sub

Publish/Subscribe architecture is not based on who is publishing or who has subscribed to receive messages. Messages are categorized into classes.
Publishers label their messages with the proper class. Subscribers receive messages depending on the classes they prefer regardless of who is publishing them.


## AWS SNS and SQS
* SNS supports several end points such as email, sms, http end point and SQS. If you want unknown number and type of subscribers to receive messages, you need SNS.

## SNS (Simple Notification Service)

   is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.

*  fast
* flexible
* fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients.
*  makes it simple and cost effective to send push notifications to mobile device users
* A distributed publish-subscribe system ,Messages are pushed to subscribers as and when they are sent by publishers to SNS ,SNS supports several end points such as email, sms, http end point and SQS.

**SQS (Simple Queue Service)**
is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later.
