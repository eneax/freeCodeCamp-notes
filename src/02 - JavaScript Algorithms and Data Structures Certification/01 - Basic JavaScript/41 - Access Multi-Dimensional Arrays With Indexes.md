# Access Multi-Dimensional Arrays With Indexes

A `multi-dimensional` array, is as an array of arrays.
If we want to access an element within a `multi-dimensional` array, we've to keep in mind that the first set of brackets refers to the `first level` array, and each additional pair of brackets refers to the next level of entries inside that particular level of array.

```js
var myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

// Select number 8
var myData = myArray[2][1];
```
