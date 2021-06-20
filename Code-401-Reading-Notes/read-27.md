# Props and State

## Review, Research, and Discussion

1. Does a deployed React application require a server?
   
   No, It doesn't 
2. Why do we prefer to test a React application at the behavior rather than the unit level?
   According to the react doc: "With components, the distinction between a “unit” and “integration” test can be blurry. If you’re testing a form, should its test also test the buttons inside of it? Or should a button component have its own test suite? Should refactoring a button ever break the form test?"
3. What does npm run build do?
   npm run build in create-react-app simply invokes some other build tool like gulp, grunt or webpack. Check your package.json to see the exact command it runs. 

4. Describe the actual composition / architecture of a React application
   Every React app has a root component of a tree of components. Some of these components are static and some have a state that could change.


   ## Term
   - BDD: Behavior-driven development is an extension of test-driven development: development that makes use of a simple, domain-specific scripting language (DSL). These DSLs convert structured natural language statements into executable tests. The result is a closer relationship to acceptance criteria for a given function and the tests used to validate that functionality. As such it is a natural extension of TDD testing in general.

   - Acceptance test: is way of writing acceptance criteria by giving examples of how software should behave in different scenarios. They are written in a standard format that promotes clarity, as well as allowing easy integration with automated testing.

   - Mounting: is the phase in which our React component mounts on the DOM (i.e., is created and inserted into the DOM). This method is called just before a component mounts on the DOM or the render method is called. After this method, the component gets mounted.

   - Build: creates a build directory with a production build of your app. Inside the build/static directory will be your JavaScript and CSS files. Each filename inside of build/static will contain a unique hash of the file contents



## Understanding React `setState`
* **setState()** is the only legitimate way to update state after the initial state setup. 
* we’re passing an object to setState(). The object contains the part of the state we want to update which ``setState({ searchTerm: event.target.value })``
* **reconciliation** process is the way React updates the DOM, by making changes to the component based on the change in state. When the request to setState() is triggered
* **Object.assign()** is used to copy data from a source object to a target object
* benifit of ``setState()``
    1. Update to a component state should be done using setState()
    2. You can pass an object or a function to setState()
    3. Pass a function when you can to update state multiple times
    4. Do not depend on this.state immediately after calling setState() and make use of the updater function instead.


## Handling Events
* React events are named using camelCase, rather than lowercase.
* With JSX you pass a function as the event handler, rather than a string.
* cannot return false to prevent default behavior in React
* When using React, you generally don’t need to call addEventListener to add listeners to a DOM element after it is created. Instead, just provide a listener when the element is initially rendered.
* can Passing Arguments to Event Handlers with the React event (e)


## Forms
* **controlled component** making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input
* **Formik** is the world's most popular open source form library for React and React Native.

## State and Lifecycle

* You can convert a function component to a class in five steps:

    1. Create an ES6 class, with the same name, that extends React.Component.
    2. Add a single empty method to it called render().
    3. Move the body of the function into the render() method.
    4. Replace props with this.props in the render() body.
    5. Delete the remaining empty function declaration.

* Adding Local State to a Class We will move the date from props to state in three steps:
 1. Replace this.props.date with this.state.date in the render() method:
 2. Add a class constructor that assigns the initial this.state:
 3. Remove the date prop from the <calssName /> element:


## Components and Props


* Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.
* define a component 

**Function and Class Components**

   1.  The simplest way to define a component is to write a JavaScript function:
```js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

This function is a valid React component because it **accepts a single “props”** (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

2. ES6 class 

**Rendering a Component**
* When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.
 
 ```js
 function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const element = <Welcome name="Sara" />;
ReactDOM.render(
  element,
  document.getElementById('root')
);
```
## The Complete Beginner's Guide to Testing React Apps
**Why React Testing Library**

Basically, React Testing Library (RTL) is made of simple and complete React DOM testing utilities that encourage good testing practices.


Almost of your tests will be written that way:

- You arrange (= setup) your code so that everything is ready for the next steps.
- You act, you perform the steps a user is supposed to do (such as a click).
- You make assertions on what is supposed to happen.
Arrange
In our test, we’ve done two tasks in the arrange part:

- Render the component
Getting the different elements of the DOM needed using queries and screen
Render
We can render our component with the render method, which is part of RTL’s API:
```js
Copy
function render(
  ui: React.ReactElement,
  options?: Omit<RenderOptions, 'queries'>
): RenderResult
```