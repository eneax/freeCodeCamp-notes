# Remove an Item from an Array

Other than adding items to a state array, we can also remove items.
For instance, we might want to remove an item from an array based on the index of that item and return a new state array with the item at the specific index removed.
Here is a possible solution using the `spread operator` and `slice()`:

```js
const immutableReducer = (state = [0, 1, 2, 3, 4, 5], action) => {
  switch (action.type) {
    case "REMOVE_ITEM":
      return [
        ...state.slice(0, action.index),
        ...state.slice(action.index + 1, state.length)
      ];
    default:
      return state;
  }
};

const removeItem = index => {
  return {
    type: "REMOVE_ITEM",
    index
  };
};

const store = Redux.createStore(immutableReducer);
```

Here is another solution using `slice()` and `concat()`:

```js
const immutableReducer = (state = [0, 1, 2, 3, 4, 5], action) => {
  switch (action.type) {
    case "REMOVE_ITEM":
      return state
        .slice(0, action.index)
        .concat(state.slice(action.index + 1, state.length));
    default:
      return state;
  }
};

const removeItem = index => {
  return {
    type: "REMOVE_ITEM",
    index
  };
};

const store = Redux.createStore(immutableReducer);
```
