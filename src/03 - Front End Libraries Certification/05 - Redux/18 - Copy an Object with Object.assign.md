# Copy an Object with Object.assign

The `state immutability` principle is applied not only when dealing with arrays, but also with objects using `Object.assign`.

The `Object.assign()` method is used to copy the values from one or more `source` objects to a `target` object.
The `target` object is the first parameter and also the value that is returned.
This method is really useful in order to create completely new objects from existing ones, while keeping the original object immutable.

Here is an example of `Object.assign()`:

```js
const myObj1 = {
  soccer: "⚽",
  football: "🏈",
  basketball: "🏀",
  volleyball: "🏐"
};

const myObj2 = myObj1;
const myObj3 = Object.assign({}, myObj1);

console.log(Object.is(myObj1, myObj2)); // true
console.log(Object.is(myObj1, myObj3)); // false
console.log(myObj3); // {soccer: "⚽", football: "🏈", basketball: "🏀", volleyball: "🏐"}
```

We can pass multiple source objects, and if there are duplicate properties in the sources, the ones passed last will win:

```js
const myObj1 = {
  soccer: "⚽",
  football: "🏈",
  basketball: "🏀",
  volleyball: "🏐"
};

const myObj2 = Object.assign({}, myObj1, {
  tennis: "🎾",
  basketball: "⛹️‍♂️"
});

console.log(myObj2); // {soccer: "⚽", football: "🏈", basketball: "⛹️‍♂️", volleyball: "🏐", tennis: "🎾"}
```

Here is an example of `Object.assign()` in Redux:

```js
const defaultState = {
  user: "eneax",
  status: "offline",
  friends: "999",
  community: "freeCodeCamp"
};

const immutableReducer = (state = defaultState, action) => {
  switch (action.type) {
    case "ONLINE":
      return Object.assign({}, state, { status: "online" });
    default:
      return state;
  }
};

const wakeUp = () => {
  return {
    type: "ONLINE"
  };
};

const store = Redux.createStore(immutableReducer);
```

The aboce code will return a new state object for actions with type `ONLINE`, which will set the `status` property to `'online'`:

```js
return Object.assign({}, state, { status: "online" });
```
