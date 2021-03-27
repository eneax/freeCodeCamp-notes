# Manipulate Arrays With unshift()

The `unshift()` method works just like `push()`, but instead of adding an element at the end of the array, it adds it at the beginning.

Example:

```js
var myArray = [
  ["John", 23],
  ["dog", 3]
];
myArray.shift();

myArray.unshift(["Paul", 35]);

console.log(myArray); // [["Paul", 35], ["dog", 3]]
```
