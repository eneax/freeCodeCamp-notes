# Selecting from Many Options with Switch Statements

The `if/else` statement is very useful to deal with more than two options.
However, when we have many options to choose from, a `switch statement` is the ideal solution.

Example:

```js
function caseInSwitch(x) {
  var answer = "";

  switch (x) {
    case 1:
      return (answer = "alpha");
      break;
    case 2:
      return (answer = "beta");
      break;
    case 3:
      return (answer = "gamma");
      break;
    case 4:
      return (answer = "delta");
      break;
    default:
      return answer;
  }
}

caseInSwitch(1);
```

The value of `x` is checked for a strict equality (`===`) to the value from the first case (`1`), then to the second (`2`) and so on.
If the equality is found, `switch` executes the code from the corresponding case, until it reaches the `break`.
