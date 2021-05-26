# Count Backwards With a For Loop

A `for loop` can also count backwards, if we modify our `initialization`, `condition`, and `final-expression`:

```js
var myArray = [];

for (var i = 9; i > 0; i -= 2) {
  myArray.push(i);
}

console.log(myArray); // [9, 7, 5, 3, 1]
```
