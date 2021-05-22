# Authentication


##  Questions:

### Explain what a “Singleton” is

A singleton is a software engineering design pattern that uses the single instance of a class to control the instantiation of objects from the class.
We can't create more than one instance of the class, and all programming operations done by the class are managed through this single instance.



### Explain how the Singleton pattern can be used with Node modules, specifically with classes

We need singleton when we want to make sure there is only one object instantiated. Therefore, instead of creating a new object we need to ensure the constructor was called only once and then we reuse the instance.

```javascript

class PrivateSingleton {
    constructor() {
        this.message = 'I am an instance';
    }
}
class Singleton {
    constructor() {
        throw new Error('Use Singleton.getInstance()');
    }
    static getInstance() {
        if (!Singleton.instance) {
            Singleton.instance = new PrivateSingleton();
        }
        return Singleton.instance;
    }
}
module.exports = Singleton;

```


### If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

create layers in middleware ( request , response and next )

Allow the middleware to have access to both layers.

Allow the middleware to end the process or move to the next middleware .

## Terms

### Router Middleware

It is a middleware that is applied to all methods done on a specific router object. Changes will apply each time the route is called by the user, modifying the requests.

### Dynamic Module Loading

Dynamic loading is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. Applications can still operate and run without these dependencies or modules, and they are only imported and injected into the application when only needed.



### Singleton Pattern

A singleton is a software engineering design pattern that uses the single instance of a class to control the instantiation of objects from the class.
We can't create more than one instance of the class, and all programming operations done by the class are managed through this single instance.

### CRUD -> REST Method Matches

It is the process when we match the HTTP request verbs with the corresponding database method done on data. So we have a GET request to read, a POST request to write, an UPDATE request to modify, a DELETE request to delete data from the database, and so on.

### Mock Testing

It is a way to perform unit tests for functions that require specific operations before and after they are called. We mock some functions to eliminate the logging effect to the console so it won't be crowded with unnecessary messages. There are many uses for mock tests, like using it to test server routes without having the server run on a specific port.


## Securing Passwords with Bcrypt Hashing Function

Passwords are the first line of defense against cyber criminals. It is the most vital secret of every activity we do over the internet and also a final check to get into any of your user account, whether it is your bank account, email account, shopping cart account or any other account you have.

**Bcrypt hash password**
bcrypt was designed for password hashing hence it is a slow algorithm. This is good for password hashing as it reduces the number of passwords by second an attacker could hash when crafting a dictionary attack.

PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM

- Brute Force attack

- Hash Collision attack




## Basic access authentication

basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request.

 In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic `<credentials>`, where credentials is the Base64 encoding of ID and password joined by a single colon :.


HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.


## Authentication Cheat Sheet
Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

**Securing Passwords with Bcrypt Hashing Function:**
- Passwords are the first defense line. For that, they must be crypt before saved in the database.
- Hash algorithms help with securing the data. although it is not reversible it can be hacked.
- Brute Force attack: While the hacker can only get hashed data. he can get the data by trying many passwords until he found one that generate the same hash pattern as the hacked password.
- Hash Collision attack: Collision is when two different input generate the same output. That is the result of having unlimited input length and predefined output length. The hacker can have the first input and try to guess the second one using the brute force attack.


**node.bcrypt.js**
A library to help you hash passwords.

Install via NPM:
 
`npm install bcrypt`

