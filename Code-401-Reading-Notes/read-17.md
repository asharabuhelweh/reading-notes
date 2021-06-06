# AWS: S3 and Lambda

## Describe “The Cloud”
 refers to servers that are accessed over the Internet, and the software and databases that run on those servers. By using cloud computing, users and companies don't have to manage physical servers themselves or run software applications on their own machines. 

## What is a container (as it relates to computers and servers)?
container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. ... Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure.
## What is auto-scaling?
Autoscaling is a cloud computing feature that enables organizations to scale cloud services such as server capacities or virtual machines up or down automatically, based on defined situations such as traffic ir utilization levels. Cloud computing providers, such as Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP), offer autoscaling tools.

## What is bandwidth?
Is the maximum data to transfer across a given path. (network bandwidth, data bandwidth).

## How do cloud providers compute service costs?
The cost is calculated based on the resources the company or individual may use in the VM in order to run their apps/services smoothly.
These recourses may be storage, processor, bandwidth and RAM.


------------------------------------------
## Term:
## Server Instances: 
is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. The details of each server instance can be viewed on the service console which can be web-based or command-line based.


## Containers:
Is a complete unit of the code (the entire runtime environment). it makes the apps run more faster and reliable from one cloud to another.

## Cloud Services:
 refers to a wide range of services delivered on demand to companies and customers over the internet. These services are designed to provide easy, affordable access to applications and resources, without the need for internal infrastructure or hardware. From checking email to collaborating on documents, most employees use cloud services throughout the workday, whether they’re aware of it or not.

**Types of Cloud Services:**
- SaaS : Software as a service. (google drive, gmail)
- Paas : platform as a service. (GitHub, Heroku, AWS Elastic beanstalk, Netlify)
- Iaas : Infrastructure as a service. (AWS EC2, Azure)

 
## Cloud Architecture
it refer to the set of softwares, applications, databases, recourses that the cloud can have to leverage its capabilities. It isn't only define the component but the relationship between them.


## AWS:
Amazon Web Services offers reliable, scalable, and inexpensive cloud computing services. Free to join, pay only for what you use.

## EC2/Beanstalk vs Heroku:
Elastic Compute cloud is a IaaS service that allow the user to control the app, data, runtime, middleware and OS
BeanStalk is a PaaS that allow the user to control only the application and the data.
Heroku is also a Paas. 


---------------------------------------------




## AWS S3: 


Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. This means customers of all sizes and industries can use it to store and protect any amount of data for a range of use cases, such as data lakes, websites, mobile applications,

  **Benefits**
  - Industry-leading performance, scalability, availability, and durability
  - Wide range of cost-effective storage classes
  - Unmatched security, compliance, and audit capabilities
  - Easily manage data and access controls
  - Query-in-place and process on-request
  - Most supported cloud storage service
 


## AWS Lambda:
**AWS Lambda** is a serverless computing service provided by Amazon Web Services (AWS). Users of AWS Lambda create functions, self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient and flexible manner.

Serverless : means You do not need to maintain your own server, but instead you use cloud services like Lambda that will take care of all the infrastructure, OS, and network layer.



**Benefits of using AWS Lambda:**
 1. Pay per use.
 2. Fully managed infrastructure. 
 3. Automatic scaling. 
 4. Tight integration with other AWS products. 


## Content Delivery Network (CDN)
![](https://cyberhoot.com/wp-content/uploads/2020/03/What-is-Content-Delivery-Network-1024x647.jpg)

Content Delivery Network is a geographically distributed group of servers that work together to provide fast delivery of Internet content. A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos.

**Benefits of using CDNs:**
 1. Increase Speed.
 2. Decrease Load on the server.
 3. Uptime.
 4. Increase server security.

**What does this mean for an SMB?**

CDNs are something that larger companies are more likely to implement. The main reasons why company want to use CDNs are to improve Internet website load speeds, content delivery speeds, and to reduce the likelihood of falling victim to and improve defenses against Distributed Denial of Service attacks (DDoS)



 A smaller company probably doesn’t need to improve website load speeds with a CDN as they typically don’t have an overwhelming amount of traffic.


