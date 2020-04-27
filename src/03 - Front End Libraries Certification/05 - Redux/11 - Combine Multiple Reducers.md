# Combine Multiple Reducers

The first Redux principle, the `store` as single source of truth, states that all app `state` is held in one single state object in the `store`.
However, as the `state` of your app grows more complex, Redux allows us to compose `reducers` in order to handle complex state models; instead of dividing the `state` into multiple pieces.

To handle different pieces of the state of our app, we define multiple `reducers` and then compose these reducers together into one `root reducer`.

In order to combine multiple reducers together, Redux provides the `combineReducers()` method. We pass as an argument to this method an object, where we define properties that associate `keys` to specific `reducers`. Then, the name we gave to the `keys` will be used by Redux to reference that particular piece of state.

```js
const rootReducer = Redux.combineReducers({
  auth: authenticationReducer,
  notes: notesReducer
});
```

As we can see from the above example, the key `auth` contains all the `state` related with authentication and handled by the `authenticationReducer`. The key `notes`, instead, contains all the `state` associated with our notes and handled by the `notesReducer`.

Finally, the `rootReducer` is passed into the Redux `createStore()` method.

A more exhaustive example of combined multiple reducers is illustrated in the code block below:

```js
const INCREMENT = "INCREMENT";
const DECREMENT = "DECREMENT";

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

const LOGIN = "LOGIN";
const LOGOUT = "LOGOUT";

const authReducer = (state = { authenticated: false }, action) => {
  switch (action.type) {
    case LOGIN:
      return {
        authenticated: true
      };
    case LOGOUT:
      return {
        authenticated: false
      };
    default:
      return state;
  }
};

const rootReducer = Redux.combineReducers({
  count: counterReducer,
  auth: authReducer
});

const store = Redux.createStore(rootReducer);
```
