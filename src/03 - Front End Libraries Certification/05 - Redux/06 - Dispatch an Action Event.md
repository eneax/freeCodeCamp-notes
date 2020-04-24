# Dispatch an Action Event

`dispatch` is a method in the `store` object that takes an `action creator` and sends the value returned from it (an `action` or object containing a `type` and sometimes a `payload`) to the Redux store.

```js
state = { login: false };

const reducer = state => state;
const store = Redux.createStore(reducer);

const action = {
  type: "LOGIN"
};
const loginActionCreator = () => {
  return action;
};

store.dispatch(loginActionCreator());
```
