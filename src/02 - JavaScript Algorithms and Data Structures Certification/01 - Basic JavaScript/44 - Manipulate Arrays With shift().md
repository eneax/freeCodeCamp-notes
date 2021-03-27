# Manipulate Arrays With shift()

The `shift()` method works just like `pop()`, except that it removes the first element from an array, instead of the last one, and then it returns it.

Example:

```js
var myArray = [
  ["John", 23],
  ["dog", 3]
];

var removedFromMyArray = myArray.shift();

console.log(removedFromMyArray); // ["John", 23]
console.log(myArray); // [["dog", 3]]
```
