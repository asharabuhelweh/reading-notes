# Redux - Asynchronous Actions


1. **How granular should your reducers be?**
-  we can separate the reducers for each component if we want to apply an action on that component , using combineReducers
2. **Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched**
- Not always we need to fire all reducer in one action dispatch

3. **Name a strategy for preventing the above**
- Make a reducer for each component that will be affected by the dispatcher, only effecting a specific amount of the state it self.

## Term 
* **store** is basically just a plain JavaScript object that allows components to share state. In a way, we can think of a store as a database. On the most fundamental level, both constructs allow us to store data in some form or another.

* the "store" is where your application state is, well, stored. The store's job is to identify the various reducers and middleware that need to be made available and used globally.


* **combineReducers** helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore . The resulting reducer calls every child reducer, and gathers their results into a single state object.

## Redux Thunk Middleware
As it turns out, Redux already has an official version of that "async function middleware", called the Redux "Thunk" middleware. The thunk middleware allows us to write functions that get `dispatch` and `getState` as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.


- By default, Redux actions are dispatched synchronously, which is a problem for any non-trivial app that needs to communicate with an external API or perform side effects. Redux also allows for middleware that sits between an action being dispatched and the action reaching the reducers.

- There are two very popular middleware libraries that allow for side effects and asynchronous actions: 
   - Redux Thunk 
   -  Redux Saga. 

**Thunk : is a programming concept where a function is used to delay the evaluation/calculation of an operation.**

`Redux Thunk` is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store’s dispatch method, which is then used to dispatch regular synchronous actions inside the function’s body once the asynchronous operations have been completed.

The most common `use` case for Redux Thunk is for **communicating asynchronously with an external API to retrieve or save data.**

- Redux Thunk makes it easy to dispatch actions that follow the lifecycle of a request to an external API.

- Redux Thunk middleware allows you to write action creators that return a function instead of an action.
  
 - The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState as parameters.
