# Bearer Authorization

## Write the following steps in the correct order

1. Ask the client if they want to sign in via a third party
2. Make a request to a third-party API endpoint
3. Redirect to a third party authentication endpoint
4. Register your application to get a client_id and client_secret
5. Receive authorization code
6. Receive access token
7. Make a request to the access token endpoint

## What can you do with an authorization code?

* enter information into a security-protected space
* Athorization

## What can you do with an access token?

Access tokens are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user's data. Access tokens must be kept confidential in transit and in storage.

## What’s a benefit of using OAuth instead of your own basic authentication?

More specifically, OAuth is a standard that apps can use to provide client applications with “secure delegated access”. OAuth works over HTTPS and authorizes devices, APIs, servers, and applications with access tokens rather than credentials.

## Terms

1. Client ID: The client_id is a public identifier for apps. Even though it’s public, it’s best that it isn’t guessable by third parties, so many implementations use something like a 32-character hex string. It must also be unique across all clients that the authorization server handles. If the client ID is guessable, it makes it slightly easier to craft phishing attacks against arbitrary applications.


2. Client Secret: is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors. Protect your client secrets and never include them in mobile or browser-based apps.


3. Authentication Endpoint: Endpoint authentication is an authentication mechanism used to verify the identity of a network's external or remote connecting device. These endpoint devices include laptops, smartphones, tablets, and servers. This method ensures that only valid or authorized endpoint devices are connected to a network. These endpoint devices include laptops, smartphones, tablets and servers.


4. Access Token Endpoint: is where apps make a request to get an access token for a user.
   
5. API Endpoint: is a point at which an application program interface (API) -- the code that allows two software programs to communicate with each other -- connects with the software program. APIs work by sending requests for information from a web application or web server and receiving a response.


6. Authorization Code:  is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.


7. Access Token: is an object encapsulating the security identity of a process or thread. A token is used to make security decisions and to store tamper-proof information about some system entity.

## JWT (JSON Web Token)

* is a JSON object encoded as a long string. We use them to identify users. It’s similar to a passport or driver’s license. It includes a few public properties about a user in its payload. These properties cannot be tampered because doing so requires re-generating the digital signature.

When the user logs in, we generate a JWT on the server and return it to the client. We store this token on the client and send it to the server every time we need to call an API endpoint that is only accessible to authenticated users.

To generate JSON Web Tokens in an Express app use jsonwebtoken package. // Generating a JWT const jwt = require(‘jsonwebtoken’); const token = jwt.sign({ _id: user._id}, ‘privateKey’);

Never store private keys and other secrets in your codebase. Store them in environment variables. Use the config package to read application settings stored in environment variables.

When appropriate, encapsulate logic in Mongoose models.

## For what should you use JSON Web Tokens?

* Authorization: allowing the user to access routes, services, and resources that are permitted with that token.
* Information Exchange : JSON Web Tokens are a good way of securely transmitting information between parties.you can be sure the senders are who they say they are


## What is the JSON Web Token structure?
In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

* Header
* Payload
* Signature