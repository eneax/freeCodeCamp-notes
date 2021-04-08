# Understanding Undefined Value returned from a Function

If we want to get an output from a function, we use the `return` keyword.
However, a function can be created also without a `return` statement. In this case, when we call the function, it'll still process the inner code but it'll return `undefined`.

Example:

```js
var sum = 0;

function addThree() {
  sum = sum + 3;
}

function addFive() {
  sum = sum + 5;
}

addThree(); // undefined
addFive(); // undefined
```
