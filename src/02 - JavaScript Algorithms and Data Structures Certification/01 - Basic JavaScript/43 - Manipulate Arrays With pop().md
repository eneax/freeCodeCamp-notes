# Manipulate Arrays With pop()

If the `push()` method adds a value at the end of an array, the `pop()` method removes an element at the end of an array and returns it.

Example:

```js
var myArray = [
  ["John", 23],
  ["Jack", 20],
  ["cat", 2]
];

var removedFromMyArray = myArray.pop();

console.log(removedFromMyArray); // ["cat", 2]
console.log(myArray); // [["John", 23], ["Jack", 20]]
```
