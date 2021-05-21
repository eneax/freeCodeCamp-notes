# Accessing Nested Arrays

Similar to accessing nested objects, we can chain `bracket` and `dot` notation to access nested arrays.

Example:

```js
var myPlants = [
  {
    type: "flowers",
    list: ["rose", "tulip", "dandelion"]
  },
  {
    type: "trees",
    list: ["fir", "pine", "birch"]
  }
];

var secondTree = myPlants[1].list[1]; // pine
```
