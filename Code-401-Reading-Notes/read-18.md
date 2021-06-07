# AWS: API, Dynamo and Lambda

### What are serverless functions?
A serverless function is a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

### If you were to create a system that emulated Lambda functions, how would you do it?
First I should write the serverless function then I need a platform that allow this service for example I can use AWS Lambda, then I need to add a trigger into another service that will invoke this function upon certain event.

### Describe how a CDN works
To minimize the distance between the visitors and your website's server, a CDN stores a cached version of its content in multiple geographical locations In essence, CDN puts your content in many places at once, providing superior coverage to your users.

## Term
### Serverless Functions

A serverless function is a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

### Cloud Storage: 
 allows you to save data and files in an off-site location that you access either through the public internet or a dedicated private network connection. Data that you transfer off-site for storage becomes the responsibility of a third-party cloud provider.

## CDN
A content delivery network, or content distribution network (CDN), is a geographically distributed network of proxy servers and their data centers. The goal is to provide high availability and performance by distributing the service spatially relative to end users.





-----------------------------------------


## Amazon API Gateway is 
Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

Many Serverless applications use Amazon API Gateway, which conveniently replaces the API servers with a managed serverless solution.

**How does API Gateway work?**

- API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends.
  
 - It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

![](https://d1.awsstatic.com/serverless/New-API-GW-Diagram.c9fc9835d2a9aa00ef90d0ddc4c6402a2536de0d.png)

### Amazon API Gateway
 **API Types**
 1. RESTful APIs
 2. WEBSOCKET APIs




## DynamoDB: 
  No-SQL database provided by AWS. key-value and document database that delivers single-digit millisecond performance at any scale.

DynamoDB is a particularly good fit for the following use cases:

  Applications with large amounts of data and strict latency requirements.
  Serverless applications using AWS Lambda.
  Data sets with simple, known access patterns.

  **Amazon DynamoDB** is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-active, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.

**Dynamoose** is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

**Key Features**

  - Type safety
  - High level API
  - Easy to use syntax
  - Ability to transform data before saving or retrieving documents
  - Strict data modeling (validation, required attributes, and more)
  - Support for DynamoDB Transactions
  - Powerful Conditional/Filtering Support
  - Callback & Promise support
