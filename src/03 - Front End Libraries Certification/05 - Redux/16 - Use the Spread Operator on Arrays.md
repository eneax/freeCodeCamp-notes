# Use the Spread Operator on Arrays

In JavaScript, the spread operator `...` has a variety of applications.
A very common use case for the spread operator is for making a new array from an existing one.
For instance, if we have an array `myArr`, we can write:

```js
let newArray = [...myArray];
```

and the `newArray` will be an exact clone of `myArray`.
In this case, both arrays will exist separately in memory. That's why, if we try to mutate `newArray` by `newArray.push(17)`, `myArray` will not be affected.

We just saw how to use the spread operator to clone an array. However, if we want to make a new copy of the array and add some additional value, we need to use the following syntax: `let myNewArr = [...myArray, 'new value']`.
Basically, it adds the string `'new value'` as the last value of the `myNewArr` array.

The code block below illustrates how to use the spread operator in a Redux reducer:

```js
const immutableReducer = (state = ["Do not mutate state!"], action) => {
  switch (action.type) {
    case "ADD_TO_DO":
      return [...state, action.todo];
    default:
      return state;
  }
};

const addToDo = todo => {
  return {
    type: "ADD_TO_DO",
    todo
  };
};

const store = Redux.createStore(immutableReducer);
```

Here, instead of mutating the state in the `immutableReducer`, we use the spread operator.
It doesn’t modify the state and it just returns a new array to which we add the action payload:

```js
return [...state, action.todo];
```
