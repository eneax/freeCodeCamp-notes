# Use Middleware to Handle Asynchronous Actions

Asynchronous actions are a fundamental part of web development and Redux provides a middleware designed specifically for this purpose, called `Redux Thunk middleware`.

In order to use `Redux Thunk middleware`, we need to pass it as an argument to `Redux.applyMiddleware()` method, which will then be provided as a second optional parameter to the `createStore()` function.

To have a better understanding of how to handle asynchronous actions in Redux, let's have a look at the example below.
Here, we're using a `setTimeout()` call to simulate the asynchronous request:

```js
// action types
const REQUESTING_DATA = "REQUESTING_DATA";
const RECEIVED_DATA = "RECEIVED_DATA";

// action creator
const requestingData = () => {
  // action without payload
  return {
    type: REQUESTING_DATA
  };
};

// action creator
const receivedData = data => {
  // action with payload
  return {
    type: RECEIVED_DATA,
    players: data.players
  };
};

// middleware
const handleAsync = () => {
  return function(dispatch) {
    dispatch(requestingData());

    setTimeout(function() {
      let data = {
        players: ["Ronaldo", "Higuain", "Dybala"]
      };
      dispatch(receivedData(data));
    }, 2500);
  };
};

const defaultState = {
  fetching: false,
  players: []
};

// reducer
const asyncDataReducer = (state = defaultState, action) => {
  switch (action.type) {
    case REQUESTING_DATA:
      return {
        fetching: true,
        players: []
      };
    case RECEIVED_DATA:
      return {
        fetching: false,
        players: action.players
      };
    default:
      return state;
  }
};

const store = Redux.createStore(
  asyncDataReducer,
  Redux.applyMiddleware(ReduxThunk.default)
);
```

In order to understand how an `async action` is created, we need to examine the `handleAsync` function.
`handleAsync` is a special action creator. It shows that we have to return a function in the `action creator` with `dispatch` as an argument.
Also, within this function, we can dispatch actions and perform asynchronous requests; while the middleware will take care of the rest.

In Redux, it's common to dispatch an action before preceding with any asynchronous request:

```js
dispatch(requestingData());
```

This allows the `state` in our application to know that some data is being requested. For instance, this is where we display some loading indicator to our users.
Then, only when we receive the data, we dispatch another action which will carry the `payload` (or the data being requested) and the information that the action is completed.

```js
setTimeout(function() {
  let data = {
    players: ["Ronaldo", "Higuain", "Dybala"]
  };
  dispatch(receivedData(data));
}, 2500);
```
