# AWS: Cloud Servers

## Review, Research, and Discussion

### Describe the Web-Request-Response-Cycle

The request/response cycle traces how a user’s request flows through the app. These are the steps of WRRC:

1. A user opens his browser, types in a URL, and presses Enter.
2. When a user presses Enter, the browser makes a request for that URL.
3. The request hits the router. The router maps the URL to the correct controller and action to handle the request.
4. The action receives the request and passes it on to the view.
5. The view renders the page as HTML.
6. The controller sends the HTML back to the browser. The page loads, and the user sees it.

### Explain what a “server” is as it relates to the WRRC?

The Server reads the Request. It knows how to read it because it is formatted as an HTTP Request.
The Server generates an HTTP Response to that Request.
The server hands the Response off to their ISP and it goes through the internet to arrive at your computer.


### What does it mean to “deploy” an application?

 putting it on a Web server so that it can be used either through the Internet or an intranet.

 ### Terms
 ### Server
SERVER is simply a computer that runs all the time and deal with requests (HTTP) and responses form clients or other servers, also sending requests to the database and back to the clients with responses.

### Pub/Sub
Publisher/ Subscribers is a messaging service that allow streaming of data from single publisher or event to multi subscribers (applications) and its asynchronous service, and stream the data in real-time and in high availability and consistent performance. 



### WRRC
Web-Request-Response-Cycle is a cycle that show the flow of data when a user or server make request to specific site then this request will go to the ISP (internet service provider) to check the DNS (Domain name server, which is basically a lot of IP addresses) and find to you the IP address of the server you are requesting then send request to that server and that server will check this request and check the databases then back with a response to your ISP and back to you with the final results.

----------------
--------------

## Virtual Machine 
type of software that will allow us to run more than one OS (operating System, is a software that allow us to control the Hardware) on the same computer! 

A virtual machine is a process of having more than one operating system and making them working inside each other as if each was an individual machine on its own.



## Cloud Computing?

is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet (“the cloud”) to offer faster innovation, flexible resources, and economies of scale.

## Amazon EC2

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure and resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. Amazon EC2’s simple web service interface allows you to obtain and configure capacity with minimal friction. It provides complete control of your computing resources and lets you run on Amazon’s proven computing environment.

