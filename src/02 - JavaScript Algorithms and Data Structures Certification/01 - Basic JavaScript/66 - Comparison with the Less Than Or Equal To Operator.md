# Comparison with the Less Than Or Equal To Operator

The `less than or equal to` operator (`<=`) compares the values of two numbers.
If the number to the left is less than or equal to the number to the right, it returns `true`.
Otherwise, it returns `false`.

The `less than or equal to` operator converts data types while comparing.

Examples:

```js
function testLessOrEqual(val) {
  if (val <= 12) {
    return "Smaller Than or Equal to 12";
  }

  if (val <= 24) {
    return "Smaller Than or Equal to 24";
  }

  return "More Than 24";
}

testLessOrEqual(10);
```
