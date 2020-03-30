# Storing Values with the Assignment Operator

Once we have declared a variable, we can store a value in it thanks to the assignment operator `=`.

```js
myFavoriteNumber = 17;
```

Here, the `Number` value 17 is assigned to the variable `myFavoriteNumber`.
Always keep in mind that assignment goes `from right to left`.

Everything standing on the right of the `=` operator is resolved before the value is assigned to the variable on the left of the operator.

```js
myVar = 17;
myNum = myVar;
```

The code above assigns 17 to `myVar`, then resolves `myVar` to 17, and finally assigns it to `myNum`.
