

# Application State with Redux
1. **What are the advantages of storing tokens in “Cookies” vs “Local Storage”**?
   - One of the biggest advantages of using tokens over cookies is the fact that token authentication is stateless. Each token contains all the data required to check its validity as well as to convey user information through claims thus making it self-contained.
2. **Explain 3rd party cookies?**
   
   - Third-party cookies are cookies that are set by a website other than the one you are currently on. For example, you can have a "Like" button on your website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites they visited.

3. **How do pixel tags work?** 
   - A tracking pixel (also called 1x1 pixel or pixel tag) is a graphic with dimensions of 1x1 pixels that is loaded when a user visits a webpage or opens an email. … The tracking pixel URL is the memory location on the server. When the user visits a website, the image with the tag is loaded from this server.


## Term
* **cookies:** Cookies are essentially pieces of code saved by websites onto the user’s web browser when a session is initiated. Cookies have a lot of uses but the most important ones are session management, user personalization, and tracking.

* **authorization**:
Authorization in system security is the process of giving the user permission to access a specific resource or function. This term is often used interchangeably with access control or client privilege.

* **access control** :Component of data security that dictates who is allowed to access and use company information and resources. Through authentication and authorization, access control policies make sure users are who they say they are and that they have appropriate access to company data.
  
  **conditional rendering** :The ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition.
Role-Based Access Control
<br>

---------

<br>

## Redux
* Redux is a library that specializes in sharing state between components using a global "Store"
  
* Redux is a predictable state container for JavaScript apps.
* The createStore factory function from Redux is used to create a Redux STORE.
* The Reducer is the only mandatory argument passed into createStore()
* A REDUCER is just a function. A function that takes in two parameters. The first is the STATE of the app, and the other is an ACTION.
* A Reducer always returns the new state of your application.
* The Initial State of your application, initialState is the second argument passed into the createStore function call.
* Store.getState() will return the current state of your application. Where Store is a valid Redux STORE.

## What it does?

Redux takes away some of the hassles faced with state management in large applications. It provides you with a great developer experience, and makes sure that the testability of your app isn’t sacrificed for any of those.

 ### Managing state with Redux requires the combination of 3 distinct aspects into a "Store" which all components can access as they please.
 - State
- Reducers (strategies to alter state)
- Actions (methods that get "dispatched" or "run", which trigger associated reducers)


## Redux Store
* Ultimately, the "store" is where your application state is, well, stored. The store's job is to identify the various reducers and middleware that need to be made available and used globally.

* React uses "reducers" to hold and manage state. Reducers typically manage just one part of the larger application state. For example, in a storefront application, you would likely have a separate reducer for Products, Categories, and Carts

## why to use Redux?

1. In larger apps with a lot of moving pieces, state management becomes a huge concern. Redux ticks that off quite well without performance concerns or trading off testability.

2. The developer experience that comes with it. Include logging, hot reloading, time travel, universal apps, record and replay
   
   ## What problem does Redux solve?
- Redux provides a solution by ensuring that: Your state is wrapped in a store which handles all updates and notifies all code that subscribes to the store of updates to the state.

  ## Who to use Redux in react? 
- create store as we create context
- pass store and context to provider
- imported as context exactly

## State Updates with Actions

* Unlike setState() in pure React, the only way you update the state of a Redux application is by dispatching an action
  
* An action is accurately described with a plain JavaScript object, but it must have a type field.
* In a Redux app, every action flows through the reducer. All of them.
  
* By using a switch statement, you can handle different action types within your Reducer.
  
* Action Creators are simply functions that return action objects.
* It is a common practice to have the major actors of a redux app live within their own folder/directory.
  
* You should not mutate the state received in your Reducer. Instead, you should always return a new copy of the state.
  
* To subscribe to store updates, use the store.subscribe() method.


## What is the best way to build applications with Redux

* It is a good practice to always plan your application development process before jumping into the code.
* In your state object, avoid nested entities at all cost. Keep the state object normalized.
* Storing your state fields as objects does have some advantages. Be equally aware of the issues with using objects, mainly the lack of order.
* The lodash utility library comes very handy if you choose to use objects over arrays within your state object.
* No matter how little, always take some time to design the state object of your application.
* With Redux, you don’t always have to pass down props. You can access state values directly from the store.
