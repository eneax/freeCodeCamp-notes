# Map Dispatch to Props

The `mapDispatchToProps()` function is used to provide our React components with specific `action creators`, so they can dispatch `actions` against the Redux `store`.

This function takes `dispatch` as a parameter and returns an object that maps `dispatch actions` to property names, which become component `props`; so that each property returns a function that calls `dispatch` with an `action creator` and any relevant action `payload`.

```js
// action creator
const addMessage = message => {
  return {
    type: "ADD",
    message: message
  };
};

const mapDispatchToProps = dispatch => {
  return {
    submitNewMessage: message => dispatch(addMessage(message))
  };
};
```

Note: Behind the scenes, react-redux is using Redux's `store.dispatch()` to dispatch actions with `mapDispatchToProps()`.
