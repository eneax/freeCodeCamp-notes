# Use a Switch Statement to Handle Multiple Actions

When we need to handle multiple actions in Redux, it's common practice to use a JavaScript `switch` statement.
The code block below shows a simple example of how to use a `reducer` to respond to two different action events: `login` and `logout`:

```js
const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {
  switch (action.type) {
    case "LOGIN":
      return {
        authenticated: true
      };
    case "LOGOUT":
      return {
        authenticated: false
      };
    default:
      return state;
  }
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: "LOGIN"
  };
};

const logoutUser = () => {
  return {
    type: "LOGOUT"
  };
};
```
