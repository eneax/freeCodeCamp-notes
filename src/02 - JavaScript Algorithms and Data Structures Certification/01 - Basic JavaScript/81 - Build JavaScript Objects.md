# Build JavaScript Objects

`Objects` represent another data type in JavaScript, which we can use to store information in a structured way.
They are similar to arrays, with the exception that, instead of using indexes to access and modify their data, we use `properties`. Shortly, we can think of objects as a `key/value` storage, similar to a dictionary.

Example:

```js
var human = {
  name: "Enea",
  age: "28",
  favoriteColors: ["black", "white"]
};
```

Moreover, we can also use `numbers` as `properties` and we can even omit the quotes for single-word string properties:

```js
var anotherObject = {
  make: "Ford",
  1: "one",
  model: "focus"
};
```
