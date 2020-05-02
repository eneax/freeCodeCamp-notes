# Extract State Logic to Redux

In order to connect React with Redux, we need to extract the local state of the stateful component into Redux.

In our previous example, we saw that the only functionality performed by the `DisplayMessages` component consists in adding a new message, typed by the user, into an unordered list. Then, all messages are displayed on the screen.

Let's see how to extract this state logic to Redux:

1. we start by defining an `action type` 'ADD':

```js
const ADD = "ADD";
```

2. we define an `action creator` (function that returns an `action` with a `type` property and a `payload`)

```js
const addMessage = message => {
  return {
    type: ADD,
    message
  };
};
```

3. then, we have to create a `reducer` that handles the state:

```js
const messageReducer = (state = [], action) => {
  switch (action.type) {
    case ADD:
      return [...state, action.type];
    default:
      return state;
  }
};
```

Remember that a `reducer` is a pure function that takes as arguments `state` and `action`, and it always returns a new state, without any side effects. Basically, the `reducer` always returns a new copy of `state` and never modifies it directly.

4. Finally, we create the `Redux store` and pass it the `reducer`:

```js
const store = Redux.createReducer(messageReducer);
```
