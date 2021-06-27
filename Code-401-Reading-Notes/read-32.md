# Custom Hooks

- **What does a component’s lifecycle refer to?**
   lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component’s existence. The definition is pretty straightforward but what do we mean by different stages? A React Component can go through four stages of its life as follows. 
 
- nitialization: This is the stage where the component is constructed with the given Props and default state. This is done in the constructor of a Component Class.
- Mounting: Mounting is the stage of rendering the JSX returned by the render method itself.
- Updating: Updating is the stage when the state of a component is updated and the application is repainted.
- Unmounting: As the name suggests Unmounting is the final step of the component lifecycle where the component is removed from the page.
  
- **Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect**

   - To prevent unnecessary re-renders
 

- **Why are functional components preferred over class components?**

  -  you don't have to think about the type of the component, will it be a class, functional, stateless
  
  - Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks. You end up with less code. They help you to use best practices.
  

- **What is wrong with the following code?**

  - useEffect is used inside a for loop, and it's not used at the top level of the function
  
    ```javascript
    import React, { useState, useEffect } from 'react';

    function MyComponent(props) {
      const [count, setCount] = useState(0);

      function changeCount(e) {
        setCount(e.target.value);
      }

      let renderedItems = [];

      for (let i = 0; i < count; i++) {
        useEffect(() => {
          console.log('component mount/update');
        }, [count]);

        renderedItems.push(<div key={i}>Item</div>);
      }

      return (
        <div>
          <input type="number" value={count} onChange={changeCount} />
          {renderedItems}
        </div>
      );
    }
    ```

---

## Terms

- **State hook**: ```useState()```, similar to ```this.setState()``` in a class except it doesn't merge the old and new state together. The only argument to ```useState()``` is the initial state. Allows us to add a state powered variable to our application.
- **Effect hook**: ```useEffect()```, adds the ability to perform side effects (data fetching, subscriptions, or manually changing the DOM from React components) from a function component. Serves the same purpose as ```componentDidMount```, ```componentDidUpdate```, and ```componentWillUnmount``` in React classes but unified into a single API. Allows us to define properties that will trigger or not trigger React API features.
- **Reducer hook**: alternative to ```useState()```, accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method (method to dispatch actions and trigger state changes per 

*  `setState `: alters the state and causes rerendering.
*  `useEffect`: used to tell React that a component needs to do something after render.  
*  `useContext`: used to create common data that can be accessed throughout the component hierarchy without passing the props down manually to each level.
*  `useToggle`: change a value between true and false.used for show and hide modal, show more/show less text, open/close side menu.
*  `useArray `:  provide various array manipulation methods like: `add()` and `removeIndex()`.
*  `react-use-form-state`:  simplify managing form state
*  `useMedia`: tracks the state of a CSS media query.
*  `usePortal`:  to render children into a DOM node that exists outside the DOM hierarchy of the parent component. 

## Custom Hooks

- Hook is a special function that lets you “hook into” React features. For example, allows you to add React state to function components.
  
- Hooks let us organize the logic inside a component into reusable isolated units
  
- Hooks apply the React philosophy (explicit data flow and composition) inside a component, rather than just between the components
  
- Hooks don’t introduce unnecessary nesting into your component tree. They also don’t suffer from the drawbacks of mixins
  Hooks let you always use functions instead of having to constantly switch between functions, classes, higher-order components, and render props

- Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in - - Hooks exposing the “building blocks” of React: state, lifecycle, and context.
  
- Built-in React Hooks like useState and useEffect serve as the basic building blocks
The only argument passed to the useState() Hook is the initial state, if you want to store two different values in state, you call useState() twice useState() returns a pair of values: the current state and a function that updates it

- Hooks are fully encapsulated — each time you call a Hook, it gets isolated local state within the currently executing component
- They’re not a way to share state — but a way to share stateful logic
  
- Each Hook may contain some local state and side effects. You can pass data between multiple Hooks just like you normally do between functions. They can take arguments and return values because they are JavaScript functions.
  
- Unlike render props or higher-order components, Hooks don’t create a “false hierarchy” in your render tree. They’re more like a flat list of “memory cells” attached to a component. No extra layers.
  
  ### Hooks API Reference
  Basic Hooks

  - useState
  - useEffect
  - useContext
  
  Additional Hooks

  - useReducer
  - useCallback
  - useMemo
  - useRef
  - useImperativeHandle
  - useLayoutEffect
  - useDebugValue
