# Define an Action Creator

Once we create an action, we need to send it to the Redux store so that it updates its state.
In Redux, this process is done by action creators, which allow us to create objects that represent action events.
An `action creator` is a JavaScript function that returns an action.

```js
const action = {
  type: "LOGIN"
};

const actionCreator = () => {
  return action;
};
```
