# Comparison with the Equality Operator

In JavaScript, the equality operator `==` compares two values and returns `true` if they're equivalent or `false` if they are not.

```js
function test(num) {
  if (num == 12) {
    return "Equal";
  }
  return "Not Equal";
}

test(10);
```

As we can see from the code above, the `test` function checks if the value of `num` is equal to `12`, and if this is `true`, it returns `Equal`. In our case, we pass the `Number` `10` to the `test` function, so it returns `Not Equal`.

Although the previous example looks pretty straight forward, there is one more thing to consider when using the `equality operator` and that's `type coercion`.
`Type Coercion` means that, if JavaScript need to compare two different data types (`numbers` and `strings`), it has to convert one type to another.

For instance:

```js
1 == 1; // true
1 == 2; // false
1 == "1"; // true
"3" == 3; // true
```

Note: keep in mind that the equality operator (`==`) is different from the assignment operator (`=`), which is used to assign the value at the `right` of the operator to a variable in the `left`.
