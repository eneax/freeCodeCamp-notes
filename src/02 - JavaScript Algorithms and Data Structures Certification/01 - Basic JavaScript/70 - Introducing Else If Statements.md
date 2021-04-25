# Introducing Else If Statements

If we have to deal with more than two possible conditions, we can chain the `if` statements together with `else if` statements.

Example:

```js
function testElseIf(val) {
  if (val > 10) {
    return "Greater than 10";
  } else if (val < 5) {
    return "Smaller than 5";
  } else {
    return "Between 5 and 10";
  }
}

testElseIf(17);
```
