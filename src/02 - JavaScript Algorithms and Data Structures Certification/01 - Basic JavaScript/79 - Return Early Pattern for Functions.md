# Return Early Pattern for Functions

When a `return` statement is reached, the execution of the current function stops.

Example:

```js
function myFunction() {
  console.log("Hello");
  return "World";
  console.log("ciaooo");
}
myFunction();
```

The above function will output `"Hello"` to the console and return `"World"`, but `"ciaooo"` is never output, since the function exits at the `return` statement.
