# Assignment with a Returned Value

When we use the assignment operator (`=`) in JavaScript, everything to the right of the equal sign is resolved before the value is assigned.

This means that we can use the value returned from a function and assign it to a variable.

Example:

```js
var mySumValue = 0;

function sum(num1, num2) {
  return num1 + num2;
}

mySumValue = sum(2, 3); // 5
```
