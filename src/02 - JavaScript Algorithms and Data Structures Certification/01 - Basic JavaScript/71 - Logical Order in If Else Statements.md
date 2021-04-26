# Logical Order in If Else Statements

When dealing with multiple conditions, the statements `if` and `else if` need to follow a particular order, depending on the result that we want to return from a function.

```js
function orderMyLogic(val) {
  if (val < 5) {
    return "Less than 5";
  } else if (val < 10) {
    return "Less than 10";
  } else {
    return "Greater than or equal to 10";
  }
}

orderMyLogic(7);
```
