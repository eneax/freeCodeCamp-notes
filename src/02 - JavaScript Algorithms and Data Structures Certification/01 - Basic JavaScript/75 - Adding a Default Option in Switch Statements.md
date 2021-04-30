# Adding a Default Option in Switch Statements

In a `switch` statement, if we have many cases to deal with and we cannot specify all of them, we can add a `default`
statement. This statement will be executed only if no matching case statements are found.

We can think of `default` as the final `else` statement in an `if/else` scenario, since both the statements are the last case.

```js
function switchOfStuff(val) {
  var answer = "";

  switch (val) {
    case "a":
      answer = "apple";
      break;
    case "b":
      answer = "bird";
      break;
    case "c":
      answer = "cat";
      break;
    default:
      answer = "stuff";
      break;
  }

  return answer;
}

switchOfStuff(1);
```
