# Comparisons with the Logical Or Operator

The logical `or` operator (`||`) returns `true` if either of the operands is `true`. Otherwise, it returns `false`.

From the example below we can see that the `testLogicalOr` function will return `"Outside"` if `val` is either less than 10 `or` greater than 20.

```js
function testLogicalOr(val) {
  if (val < 10 || val > 20) {
    return "Outside";
  }

  return "Inside";
}

testLogicalOr(15);
```
