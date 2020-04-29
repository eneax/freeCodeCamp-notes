# Never Mutate State

One of the core principles of Redux is that `state` is `immutable`.
It means that we can never modify `state` directly. What we do, instead, is return a new copy of state.

```js
// action type
const ADD_TO_DO = "ADD_TO_DO";

// A list of strings representing tasks to do:
const todos = [
  "Go to the store",
  "Clean the house",
  "Cook dinner",
  "Learn to code"
];

const immutableReducer = (state = todos, action) => {
  switch (action.type) {
    case ADD_TO_DO:
      // don't mutate state here
      return todos.concat(action.todo);
    default:
      return state;
  }
};

const addToDo = todo => {
  return {
    type: ADD_TO_DO,
    todo
  };
};

const store = Redux.createStore(immutableReducer);
```

In the above code block represents a simple example where, instead of mutating the state in the `immutableReducer`,
we use the JavaScript `.concat()` array method which doesn’t modify the array and it returns a new array to which we add the action payload:

```js
return todos.concat(action.todo);
```
