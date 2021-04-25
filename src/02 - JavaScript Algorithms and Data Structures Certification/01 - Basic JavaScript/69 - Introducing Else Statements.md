# Introducing Else Statements

An `if/else` statement gives us the possibility to return two separate code blocks.
When a condition for an `if` statement is `true`, the first code block is executed.
If, however, the condition is `false`, an alternate code block will execute instead of the first code block.

Example:

```js
function testElse(val) {
  var result = "";

  if (val > 5) {
    result = "Bigger than 5";
  } else {
    result = "5 or Smaller";
  }

  return result;
}

testElse(4);
```
