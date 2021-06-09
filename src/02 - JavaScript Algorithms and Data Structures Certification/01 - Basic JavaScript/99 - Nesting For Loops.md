# Nesting For Loops

Sometimes, the data that we want to access is deeply nested into a `multi-dimensional array`.
In that case, we have to loop through both the array and any sub-arrays.

Example:

```js
function multiplyAll(arr) {
  var product = 1;

  for (var i = 0; i < arr.length; i++) {
    for (var j = 0; j < arr[i].length; j++) {
      product *= arr[i][j];
    }
  }

  return product;
}

multiplyAll([
  [1, 2],
  [3, 4],
  [5, 6, 7]
]); // 5040
```
