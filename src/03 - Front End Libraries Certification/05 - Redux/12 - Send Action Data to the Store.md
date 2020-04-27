# Send Action Data to the Store

We've seen how to dispatch an action to the Redux store, but so far these actions have contained only a `type` property.
With our actions, we can send also a `payload` of information, which is related to the data that the user generates when interacting with our application.

```js
// action type
const ADD_NOTE = "ADD_NOTE";

// reducer
const notesReducer = (state = "Initial State", action) => {
  switch (action.type) {
    case ADD_NOTE:
      return action.text;
    default:
      return state;
  }
};

// action creator
const addNoteText = note => {
  return {
    // action
    type: ADD_NOTE,
    text: note
  };
};

const store = Redux.createStore(notesReducer);

console.log(store.getState());
store.dispatch(addNoteText("Hello!"));
console.log(store.getState());
```
