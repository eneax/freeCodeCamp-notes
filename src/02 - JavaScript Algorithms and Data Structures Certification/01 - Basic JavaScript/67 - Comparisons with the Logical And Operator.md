# Comparisons with the Logical And Operator

The logical `and` operator (`&&`) returns `true` if and only if the operands to the left and right of it are `true`.
This operator is very useful when we need to compare more than one thing at a time.

As we can see from the example below, the `testLogicalAnd` function will return `"Yes"` if and only if the `val` value is between 25 and 50:

```js
function testLogicalAnd(val) {
  if (val >= 25 && val <= 50) {
    return "Yes";
  }

  return "No";
}

testLogicalAnd(10);
```
