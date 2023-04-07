## What is Redux?
```
1. Redux is a state management library for JavaScript applications. 
2. Redux is based on the concept of a single "store" that holds the entire state of the application
3. This store is a plain JavaScript object that can only be modified by dispatching "actions" to it
```

## what is reducer
1. In redux, the reducers are the pure functions that contain the logic and calculation that needed to be performed on the state. 
2. These functions accept the initial state of the state being used and the action type. It updates the state and responds with the new state.
3. When an action is dispatched, it triggers a "reducer" function that takes the current state and the action as inputs, and returns a new state that reflects the changes described by the action. Reducers are pure functions that do not modify the original state, but rather return a new state object.

## What are actions
 Actions are JavaScript object that contains information. Actions are the only source of information for the store.
 An action is a plain JavaScript object that describes a change to the state of the application, such as adding a new item to a list or updating a user's profile.
 ```
 const Actions = {
 type: '',
 payload: ''
}
```
## Explain the flow of redux.
1. The application state is stored in a single object called the store. The store is created by combining multiple reducers, which are pure functions that take the current state and an action as input and return a new state.
2. To update the state, an action is dispatched to the store. An action is a plain JavaScript object that has a type property and optionally other data that can be used to update the state.
3. The store calls the appropriate reducer based on the action's type property, and passes the current state and the action as input.
4. The reducer returns a new state based on the current state and the action.
5. The store updates its state with the new state returned by the reducer, and notifies all subscribers that the state has changed.
6. The subscribers, typically components in a React application, can access the new state from the store and re-render the user interface based on the new data.
