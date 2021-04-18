# Comparison with the Greater Than Operator

The greater than operator (`>`) compares the values of two numbers and returns `true` if the number to the left is greater than the number to the right. Otherwise, it returns `false`.

Just like the `equality operator`, also `greater than` operator converts data types of values while comparing.

Examples:

```js
function testGreaterThan(val) {
  if (val > 100) {
    return "Over 100";
  }

  if (val > 10) {
    return "Over 10";
  }

  return "10 or Under";
}

testGreaterThan(10);
```
