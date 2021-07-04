# Combined Reducers



 1. **Why choose Redux instead of the Context API for global state?**
- We use Redux for managing the state of large & complicated applications. It is more efficient for larger projects because the context API re-renders more often and suit more the simple state like change the theme or the language.

 1. What is the purpose of a reducer?
     - reducer are pure functions that implement the action behavior. They take the current application state, perform an action, and then return a new state.

    - We need reducers to tell the application how to change state in response to an action. The action does not do anything except describe what happened and it is up to the reducer to respond to this.

 1. **does an action contain?**
    - These are objects that are used to send data to the Redux store.

    - They typically have two properties: a **type** property for describing what the action does and a **payload** property that contains the information that should be changed in the app state.

 4. **Why do we need to copy the state in a reducer?**
    - redux only requires our reducers to stay `pure`. If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part.
  
  ## Term 

  - **immutable state**
    - Immutability is a concept that React programmers need to understand. An immutable value or object cannot be changed, so every update creates new value, leaving the old one untouched.
    - Means that it read-only, to ensure that it only changes through actions in reducers

- **time travel in redux**
  - Time travel is the ability to move back and forth among the previous states of an application and view the results in real time. 
  - With Redux, given a specific state and a specific action, the next state of the application is always exactly the same. Redux is a predictable state container and it easy to implement time travel with it.

- **action creator**
  - A function that returns an action object. Redux includes a utility function called bindActionCreators for binding one or more action .

- **reducer**
  - These are pure functions that implement the action behavior. They take the current application state, perform an action, and then return a new state

- **dispatch**
  - dispatch is a function of the Redux store. You call store. dispatch to dispatch an action. This is the only way to trigger a state change. With React Redux, your components never access the store directly - connect does it for you.
  
  ----
## Combined Reducers
  **Why we use Combined Reducers**?

-  When the application grows **bigger**, the number of states that we want to maintain the user experience and the whole workflow of the application also increases.
-  Therefore, we tend to **create multiple reducers** for each state instead of making one giant reducer that holds all the information and the functions we want to execute.

- `combineReducers` is simply a utility function to simplify the most common use case when writing Redux reducers. 

- Redux solved this problem by introducing the `combineReducer({reducer_1,reducer_2,...})` function. 
  
- This function takes multiple reducers as an object argument and return one single reducer that manages all the dispatch actions from it.
  
```js
  // reducers.js
export default theDefaultReducer = (state = 0, action) => state

export const firstNamedReducer = (state = 1, action) => state

export const secondNamedReducer = (state = 2, action) => state

// rootReducer.js
import { combineReducers, createStore } from 'redux'

import theDefaultReducer, {
  firstNamedReducer,
  secondNamedReducer
} from './reducers'

// Use ES6 object literal shorthand syntax to define the object shape
const rootReducer = combineReducers({
  theDefaultReducer,
  firstNamedReducer,
  secondNamedReducer
})

const store = createStore(rootReducer)
```
  
-  What happens when we dispatch an action is that combineReducer invokes all the reducers at once giving each reducer a chance to respond to the action being dispatched. This behavior is somehow not so efficient but it gets the job done, and it will retain the consistency of the whole application work flow.


## combineReducers(reducers)
- As your app grows more complex, you'll want to split your reducing function into separate functions, each managing independent parts of the state.
  
- The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

- The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by combineReducers() namespaces the states of each reducer under their keys as passed to combineReducers()

`Arguments`
- reducers (Object): An object whose values correspond to different reducing functions that need to be combined into one. See the notes below for some rules every passed reducer must follow.

`Returns`
- (Function): A reducer that invokes every reducer inside the reducers object, and constructs a state object with the same shape.