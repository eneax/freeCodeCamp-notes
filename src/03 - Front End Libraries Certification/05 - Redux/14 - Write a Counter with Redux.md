# Write a Counter with Redux

Here's an example of how to build a simple counter with Redux:

```js
// action types
const INCREMENT = "INCREMENT";
const DECREMENT = "DECREMENT";

// counter reducer which increments or decrements the state based on the action it receives
const counterReducer = (state = 0, action) => {
  switch (action.type) {
    case INCREMENT:
      return state + 1;
    case DECREMENT:
      return state - 1;
    default:
      return state;
  }
};

// action creator for incrementing state
const incAction = () => {
  return {
    type: INCREMENT
  };
};

// action creator for decrementing state
const decAction = () => {
  return {
    type: DECREMENT
  };
};

// define Redux store and pass in reducers
const store = Redux.createStore(counterReducer);
```
