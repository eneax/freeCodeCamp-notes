# Use Conditional Logic with If Statements

Every time we have to make a decision in our JavaScript code, we use to `if` keyword.
It tells JavaScript to execute the code defined in the curly braces if a certain condition is met.

These conditions are known as `Boolean conditions` and they can have only two values: `true` or `false`.

Example:

```js
function trueOrFalse(wasThatTrue) {
  if (wasThatTrue) {
    return "Yes, that was true";
  }
  return "No, that was false";
}
```

As we can see from the example above, `wasThatTrue` is `true` so our `trueOrFalse` function will return the string `"Yes, that was true"`.
The second `return` statement `"No, that was false"` will not execute.
