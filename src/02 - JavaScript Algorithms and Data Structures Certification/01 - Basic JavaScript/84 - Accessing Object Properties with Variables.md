# Accessing Object Properties with Variables

When dealing with objects, we can use bracket notation to access a property which is stored as the value of a variable.
This can be extremely useful when iterating through an object's properties.

Example:

```js
var juve = {
  7: "Ronaldo",
  9: "Higuain",
  10: "Dybala"
};

var playerNumber = 7;
var player = juve[playerNumber]; // "Ronaldo"
```
