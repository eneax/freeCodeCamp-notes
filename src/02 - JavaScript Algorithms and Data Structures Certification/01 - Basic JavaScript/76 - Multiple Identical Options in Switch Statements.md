# Multiple Identical Options in Switch Statements

If we omit the `break` statement from a switch statement's case, the `case`s will execute until a `break` is encountered.

This can be a handy solution if we have multiple identical options that we might prefer to group together.

Example:

```js
function sequentialSizes(val) {
  var answer = "";

  switch (val) {
    case 1:
    case 2:
    case 3:
      answer = "Low";
      break;
    case 4:
    case 5:
    case 6:
      answer = "Mid";
      break;
    case 7:
    case 8:
    case 9:
      answer = "High";
      break;
  }

  return answer;
}

sequentialSizes(1);
```
