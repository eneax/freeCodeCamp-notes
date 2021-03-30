# Local Scope and Functions

When a variable is declared within a function, it has a `local scope`. Thus, it will only be visible within that particular function.

Example:

```js
function myLocalScope() {
  var myName = "Enea";
  console.log(myName);
}
myLocalScope(); // "Enea"

console.log(myName); // Uncaught ReferenceError: myName is not defined
```
