# Replace Loops using Recursion

Recursion is the concept that a function can be expressed in terms of itself, so that we don't need to use a loop.

Example:

```js
function sum(arr, n) {
  if (n <= 0) {
    return 0;
  } else {
    return sum(arr, n - 1) + arr[n - 1];
  }
}

sum([2, 3, 4, 5], 3); // 9
```
