# Global vs. Local Scope in Functions

We might come across a case in which we have both a local and a global variable with the same name. In this scenario, the local variable prevails over the global variable.

Example:

```js
var clothes = "T-Shirt";

function myOutfit() {
  var clothes = "Sweater";

  return clothes;
}

myOutfit(); // "Sweater"
```
