# Global Scope and Functions

In JavaScript, `scope` represents the visibility of a variable.

If a variable is defined outside of a function block, it has a `Global scope`, and it can be seen everywhere in our code.
If we use a variable without the `var` keyword, it'll also be created automatically in the global scope. This can lead to some unintended consequences in our code so it's important to always declare variables with `var`.

In the example below, we can see that the variable `myGlobalVariable` is defined outside a function and therefore it belongs to the global scope.
Moreover, also the `anotherGlobalVariable` inside the function `functionOne()` belongs to the global scope, since it has been declared without using the `var` keyword.

Considering that both the variables are defined in the global scope, they can be accessed everywhere in our code, that this is why the function `functionTwo()` has access to them.

```js
var myGlobalVariable = 10;

function functionOne() {
  anotherGlobalVariable = 5;
}

function functionTwo() {
  var output = "";
  if (typeof myGlobalVariable != "undefined") {
    output += "myGlobalVariable: " + myGlobalVariable;
  }
  if (typeof anotherGlobalVariable != "undefined") {
    output += " anotherGlobalVariable: " + anotherGlobalVariable;
  }
  console.log(output); // myGlobalVariable: 10 anotherGlobalVariable: 5
}
```

Note: In JavaScript, we use the `typeof` operator to check the type of a variable.
