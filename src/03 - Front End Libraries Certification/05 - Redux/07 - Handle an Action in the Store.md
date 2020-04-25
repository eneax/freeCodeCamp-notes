# Handle an Action in the Store

Once the action is created and dispatched, the Redux `store` needs to respond to that action by modifying the `state`.
This job is done by `reducers`. A `reducer` is a pure function that takes as arguments: `state` and `action` and it always returns a new state, without any side effects.

One important thing to remember, when handling an action in the store, is that `state` is read-only. Basically, the `reducer` must always return a new copy of `state` and never modify it directly.

```js
const defaultState = {
  login: false
};

const reducer = (state = defaultState, action) => {
  if (action.type === "LOGIN") {
    return {
      login: true
    };
  } else {
    return state;
  }
};

const store = Redux.createStore(reducer);

const action = {
  type: "LOGIN"
};
const loginActionCreator = () => {
  return action;
};

store.dispatch(loginActionCreator());
```

In the example above, we can see that dispatching the action creator `loginAction` will update the `login` property in the `store` state to `true`.
