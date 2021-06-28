# Context API


1. Describe use cases for ``useMemo()`` and ``useReducer()``?
- **useMemo** is a React hook that memorizes the output of a function
- **useReducer** is usually preferable to useState when you have complex state  logic that involves multiple sub-values or when the next state depends on the previous one

2. Why do custom hooks need the use prefix?
- Should start with use so that you can tell at a glance that the rules of Hooks apply to it.
- also both components and hooks are JS function so it's a way to differentiate between them.
- Custom hooks are normal JS functions, named with the prefix ‘use’, that can use hooks inside of it and contain a common stateful logic to be reused in other components.

3. What do custom hooks usually do?
- Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks


4. Using any list of custom hooks, research and name one that you think will be useful in your applications
    
   * useWebSocket would be useful when building a game web app that needs to communicate with a websocket api. 
   *  react-fetch-hook.


1. Describe how a hook that fetches API data might work
We could abstract the logic for fetching the data into a custom hook then call that in useEffect for example on multiple pages if they all need access to data from that api cal

## Term 
- reducer: A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change.

----

## Context API

* Context API is a (kind of) new feature added in version 16.3 of React that allows one to share state across the entire app (or part of it) lightly and with ease
  
*  Context API is a way for a React app to effectively produce global variables that can be passed around, it's   alternative to "prop drilling" or moving props from grandparent to child to parent, and so on.
  

*  don't pass down the Avatar component itself so that the intermediate components don’t need to know about the  props=====>  only the top-most Page component need to know 


* **Benefit**
 1. make your code cleaner in many cases by reducing the amount of props you need to pass through your application 
 2. giving more control to the root components


Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.

## When to Use Context

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.
Using context, we can avoid passing props through intermediate elements.

Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

## Context APIs

### React.createContext

Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This default value can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.

### Context.Provider

Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.

The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.

All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes. The propagation from Provider to its descendant consumers (including .contextType and useContext) is not subject to the shouldComponentUpdate method, so the consumer is updated even when an ancestor component skips an update.

Changes are determined by comparing the new and old values.

### Class.contextType

The contextType property on a class can be assigned a Context object created by React.createContext(). Using this property lets you consume the nearest current value of that Context type using this.context. You can reference this in any of the lifecycle methods including the render function. It can only subscribe to a single context using this API.

### Context.Consumer

A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

Requires a function as a child. The function receives the current context value and returns a React node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree. If there is no Provider for this context above, the value argument will be equal to the defaultValue that was passed to createContext().

## Updating Context from a Nested Component

It is often necessary to update the context from a component that is nested somewhere deeply in the component tree. In this case you can pass a function down through the context to allow consumers to update the context.

## Consuming Multiple Contexts

To keep context re-rendering fast, React needs to make each context consumer a separate node in the tree.

If two or more context values are often used together, you might want to consider creating your own render prop component that provides both.


* **Creates a Context object** ``const MyContext = React.createContext(defaultValue)`
* When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.
* The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. 
 1. ``Context.Provider`` ===> ``<MyContext.Provider value={/* some value */}>``
 2. ``Class.contextType``
 3. ``Context.Consumer``
 4. ``Context.displayName``




