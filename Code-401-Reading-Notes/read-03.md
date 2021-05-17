# Express REST API

## Name 3 real-world use cases where you’d want to change the request with custom middleware?

1. Using `express.urlencoded` to parse the request body from forms.
2. Using authentication middlewares 
3. Using cookie parser

## True or false: The route handler is middleware?
false


## In what ways can a middleware function end the process and send data to the browser?

by calling the next function with an argument or throw and error, we would end the middleware sequence.

## At what point in the request lifecycle can you “inject” middleware?

* We can inject the middleware globally using `app.use(middleware)`. Here, the middleware will be executed to perform actions on all routes and methods. It will be the first thing to run in the method handler.
* We can also inject it between the route path and the method handler inside each route we create. It will only apply to the handler that it was injected in.

## What can cause express to throw an error with “Request headers sent twice, cannot start a second response.”

If one of the middleware items writes to the response body or headers but doesn't call `response.end()` and you call `next()`, then as the core Server.prototype.handle method completes, it's going to notice that:

* no more items in the stack
* that `response.headerSent` is true

## Terms

1. Middleware: it is a script that contains some code or functions that modify the behavior of the method handler. It manipulates the request and adds some more functionality to the overall callback.
2. Request Object: It is passed to the route handler by default, and it contains different properties that determine the request behavior. It contains data like the headers, the request's path, the request's body, the URL to hit, and more.
3. Response Object: it is a default object passed to the route handler argument list. It contains the response from the server and how it should be sent to the user. It contains data like status code, response body, URL, server address, and more.
4. Application Middleware: they are middlewares that are applied to the whole application, and they will be called every time a route is hit or a request being sent.
5. Routing Middleware: they are middlewares added to a specific route or group of routes and method handlers. They only modify the routes and methods they are injected in, not all routes.
6. Test-Driven Development: it is a programming style that ensures that the application we build is working properly without problems. The results that are delivered to the clients are of high quality. It requires performing a different test to the application's functionalities called the unit tests, which means that we should test all functions and pieces of code of our application with all possible cases that the user might encounter during dealing with the application.
7. Behavioral Testing: Behavioral Testing is a testing of the external behavior of the program, also known as black-box testing. It is usually functional testing. It is a branch of Test Driven Development (TDD). BDD uses human-readable descriptions of software user requirements as the basis for software tests.

## Preparation Materials

**Classes**
Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

**Defining classes**
Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations.


***Class declarations***
One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the class ("Rectangle" here).

```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```
**Sub classing with extends**
The extends keyword is used in class declarations or class expressions to create a class as a child of another class.
```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name); // call the super class constructor and pass in the name parameter
  }

  speak() {
    console.log(`${this.name} barks.`);
  }
}

let d = new Dog('Mitzie');
d.speak(); // Mitzie barks.
```
