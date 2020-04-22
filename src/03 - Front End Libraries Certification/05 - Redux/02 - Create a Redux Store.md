# Create a Redux Store

Redux is a state management framework that can be used with different UI libraries, including React.

The main feature of Redux, is the idea of storing the entire state of our application into `a single state object`.
That's why when it comes to application state, the Redux store is the `single source of truth`.
It means that any time a component wants to update the state, it must do it only through the Redux store.
This unidirectional data flow makes it much easier to manage state in our app.

Basically, the Redux store is an `object` that holds and manages the application state.
We create the Redux store by calling `createStore()`, a method on the Redux object, and passing it a `reducer` function as an argument.

A `reducer` is a function that takes state as an argument and returns state.

```js
const reducer = (state = 17) => {
  return state;
};

// Define the store
const store = Redux.createStore(reducer);
```

In the example above, we used `ES6 default argument` syntax to initialize this state to hold a value of 17.
