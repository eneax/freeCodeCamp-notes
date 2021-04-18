# Comparison with the Greater Than Or Equal To Operator

The `greater than or equal to` operator (`>=`) compares the values of two numbers.
If the number to the left is greater than or equal to the number to the right, it returns `true`. Otherwise, it returns `false`.

The `greater than or equal to` operator converts data types while comparing.

Example:

```js
function testGreaterOrEqual(val) {
  if (val >= 20) {
    return "20 or Over";
  }

  if (val >= 10) {
    return "10 or Over";
  }

  return "Less than 10";
}

testGreaterOrEqual(10);
```
