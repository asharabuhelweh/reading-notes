# Component Composition
## Review, Research, and Discussion

1. ### Can a parent component access the state of a child component?
    In React we can access the child’s state using Refs.  we will assign a Refs for the child component in the parent component. then using Refs we can access the child’s state.

Creating Refs Refs are created using React.createRef() and attached to React elements via the ref attribute.

2. ### What can be passed along in a prop variable?**
 We can pass any data type and also we can pass functions. 

3. ### How can a child component “know” the state of another component?

To obtain the state of another component, you can pass the component's state to it's child components as props. You can also have components share a common ancestor, and have them access the same state in a similar manner.

## Term
- **Component Props**: Keyword in React for properties, can be any information, function, JavaScript that needs to be passed to another component. Can only be passed in one direction, from the root to its children, no way for data to be passed up.

- **Component State**: React components have built in state object, which is where you stor property values that belong to the component. When the state object changes, t he component re-renders. 
 - **Application State**: In an application, state is interface between data (from backend or local change) and the representation of this data with UI elements on the front-end. State is able to keep the data of different components in sync because each state update will re render all relevant components. State can be a medium to communicate between different components as well.

## The Component Lifecycle
**The lifecycle methods allow us to run code at specific points in the component’s life or in response to changes in the component’s life.**
![](https://cdn-media-1.freecodecamp.org/images/1*U13Mlxz_ktcajaeJCyYkwg.png)

1. **Mounting**
* first method that runs is the constructor method
* render method which returns JSX
* ``componentDidMount`` inside of it we ca do any asynchronous calls to databases or directly manipulate the DOM 


2. **Updating** 
* call ``getDerivedStateFromProps``
* ``getDerivedStateFromProps`` you can compare old props/state with the new set of props/state. You can determine if your component should re-render or not by returning true or false
* ``getSnapshotBeforeUpdate``  It allows the engineer to capture some information about the DOM before it's changed

3. **Unmounting**
* this phase is that last stage of the component lifecycle. When you remove a component from the DOM, React runs ``componentWillUnmount`` right before it gets removed. You should use this method to clean up any open connections such as WebSockets or intervals.

### Other Lifecycle Methods
- **forceUpdate** is a method that directly causes a re-render. While there may be a few use cases for it, it should typically be avoided.
  
- **getDerivedStateFromError** on the other hand is a lifecycle method that isn’t directly part of the component lifecycle. In the event of an error in a component, getDerivedStateFromError runs and you can update state to reflect that an error occurred. Use this method copiously.


## Higher-Order Components(HOC)
  A higher-order component is a function that takes a component and returns a new component.
* When we call **connect**, we get a HOC back that we can use to wrap a component
* HOCs allow us to do is abstract shared logic between components into a single overarching component.
* A good use case for an HOC is authorization. You could write your authentication code in every single component that needs it. It would quickly and unnecessarily bloat your code.
  

**React State and setState()**: method The only way you should change state

- when there’s a state change, React will trigger a re-render on that component (unless you specify in shouldComponentUpdate to say otherwise).
- 
Now let’s talk about how we change state. The only way you should change state is via the setState method. This method takes an object and merges it into the current state. 

**React Context**

The React context API allows you to create global context objects that can be given to any component you make. This allows you to share data without having to pass props down all the way through the DOM tree.

## props.children
What is ‘children’?
My simple explanation of what this.props.children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.

* **stateless function** is just a plain javascript function which takes props as an argument and returns a react element, and there is no ``this`` keyword 
* we use props.children on components that represent '‘'generic boxes' 

## composition & inheritance
* recommend  use composition instead of inheritance to reuse code between components.


**Composition vs Inheritance**
- React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.
  
- Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. Remember that components may accept arbitrary props, including primitive values, React elements, or functions.
  
- If you want to reuse non-UI functionality between components, we suggest extracting it into a separate JavaScript module. The components may import it and use that function, object, or a class, without extending it.
  
-  React does not say Composition is better than Inheritance. Composition just fits better within the React's component structure. ... With the addition of the latest Hooks in React, re-using code is only going to be much easier