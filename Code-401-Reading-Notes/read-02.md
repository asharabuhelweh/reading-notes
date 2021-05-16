**what is the difference between PUT and PATCH?**
The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.

PUT is a method of modifying resource where the client sends data that updates the entire resource. PATCH is a method to apply a partial update to the resource.

**Provide links to 3 services or tools that allow you to “mock” an API?**
1. [Nock]([Nock](https://github.com/nock/nock))
2. [MockServer](http://www.mock-server.com/)
3. [Beeceptor](https://beeceptor.com/)
   
**Compare and contrast SOAP and ReST**


KEY DIFFERENCE
- SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.
- SOAP is a protocol whereas REST is an architectural pattern.
- SOAP uses service interfaces to expose its functionality to client applications while - - REST uses Uniform Service locators to access to the components on the hardware device.
- SOAP needs more bandwidth for its usage whereas REST doesn’t need much bandwidth.
- SOAP only works with XML formats whereas REST work with plain text, XML, HTML and JSON.
SOAP cannot make use of REST whereas REST can make use of SOAP.

**Compare and contrast Swagger and APIDoc.js**
  

* apiDocjs: Inline Documentation for RESTful web APIs. It creates a documentation from API annotations in your source code. It includes a default template which uses handlebars, Bootstrap, RequireJS and jQuery for the output of the generated apidata.js and apiproject.js as a html-page; 
  
* Swagger Inspector: Test and Document Your APIs With Ease. It is a free cloud-based API testing and documentation tool to simplify the validation of any API and generate its corresponding OpenAPI documentation.

apiDocjs and Swagger Inspector can be primarily classified as "API" tools.

apiDocjs is an open source tool with 7.71K GitHub stars and 1.36K GitHub forks. Here's a link to apiDocjs's open source repository on GitHub.

   
# Express/Node introduction

Node is an open-source, cross-platform runtime environment that allows developers to create all kinds of server-side tools and applications in JavaScript. The runtime is intended for use outside of a browser context (i.e. running directly on a computer or server OS). As such, the environment omits browser-specific JavaScript APIs and adds support for more traditional OS APIs including HTTP and file system libraries.

**From a web server development perspective Node has a number of benefits:**

* Great performance! Node was designed to optimize throughput and scalability in web applications and is a good solution for many common web-development problems (e.g. real-time web applications).

* Code is written in "plain old JavaScript", which means that less time is spent dealing with "context shift" between languages when you're writing both client-side and server-side code.

 * JavaScript is a relatively new programming language and benefits from improvements in language design when compared to other traditional web-server languages (e.g. Python, PHP, etc.) Many other new and popular languages compile/convert into JavaScript so you can also use TypeScript, CoffeeScript, ClojureScript, Scala, LiveScript, etc.
  
* The node package manager (NPM) provides access to hundreds of thousands of reusable packages. It also has best-in-class dependency resolution and can also be used to automate most of the build toolchain.


* Node.js is portable. It is available on Microsoft Windows, macOS, Linux, Solaris, FreeBSD, OpenBSD, WebOS, and NonStop OS. Furthermore, it is well-supported by many web hosting providers, that often provide specific infrastructure and documentation for hosting Node sites.
  
* It has a very active third party ecosystem and developer community, with lots of people who are willing to help.


## Introducing Express
Express is the most popular Node web framework, and is the underlying library for a number of other popular Node web 
frameworks. It provides mechanisms to:

1. Write handlers for requests with different HTTP verbs at different URL paths (routes).
2.  Integrate with "view" rendering engines in order to generate responses by inserting data into templates.
3. Set common web application settings like the port to use for connecting, and the location of templates that are used for rendering the response.
4. Add additional request processing "middleware" at any point within the request handling pipeline.

# npm 
is the world's largest software registry. Open source developers from every continent use npm to share and borrow packages, and many organizations use npm to manage private development as well.

npm consists of three distinct components:

* the website
* the Command Line Interface (CLI)
* the registry

**Use npm to:**
- Adapt packages of code for your apps, or incorporate packages as they are.
- Download standalone tools you can use right away.
- Run packages without downloading using npx.
Share code with any npm user, anywhere.
- Restrict code to specific developers.
- Create organizations to coordinate package maintenance, coding, and developers.
- Form virtual teams by using organizations.
- Manage multiple versions of code and code dependencies.
- Update applications easily when underlying code is updated.
- Discover multiple ways to solve the same puzzle.
- Find other developers who are working on similar problems and projects.


## TDD
Definition
“Test-driven development” refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).

**Expected Benefits**
- many teams report significant reductions in defect rates, at the cost of a moderate increase in initial development effort
* the same teams tend to report that these overheads are more than offset by a reduction in effort in projects’ final phases
- although empirical research has so far failed to confirm this, veteran practitioners report that TDD leads to improved design qualities in the code, and more generally a higher degree of “internal” or technical quality, for instance improving the metrics of cohesion and coupling



