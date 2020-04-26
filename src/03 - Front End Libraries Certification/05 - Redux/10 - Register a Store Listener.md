# Register a Store Listener

In Redux, we can subscribe listener functions to the `store` using `store.subscribe()`.
Listener functions are called anytime an action is dispatched against the store.

In the example below, we can see how the `subscribe()` method is used to log a message whenever an action is received and the `store` is updated.

```js
const ADD = "ADD";

const reducer = (state = 0, action) => {
  switch (action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};

const store = Redux.createStore(reducer);

// global count variable:
let count = 0;

// callback function
const addOne = () => count++;

// subscribe listener function
store.subscribe(addOne);

store.dispatch({ type: ADD });
console.log(count); // 1

store.dispatch({ type: ADD });
console.log(count); // 2

store.dispatch({ type: ADD });
console.log(count); // 3
```

Note: A `callback function` is just a function that get’s called after another function is done being executed.
