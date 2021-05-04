# Accessing Object Properties with Bracket Notation

The second way to access the properties of an object is using bracket notation (`[]`).
Bracket notation is extremely useful when the property of the object we are trying to access has a space in its name.

Example:

```js
var menu = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};

var entreeValue = menu["an entree"];
var sideValue = menu["my side"];
var drinkValue = menu["the drink"];
```
