# Iterate with JavaScript For Loops

The most common type of JavaScript loop is the `for loop`. It runs "for" a specific number of times.

`For loops` are made of three expressions separated by semicolons:

```js
for ([initialization]; [condition]; [final-expression])
```

The `initialization` statement is executed only once, just before the loop starts, in order to define and setup the loop variable.

The `condition` statement runs at the beginning of every loop iteration and will continue as long as it evaluates to `true`. When condition becomes `false` at the start of the iteration, the loop will stop executing.
That's why a loop will never execute if `condition` starts as false.

The `final-expression` is executed at the end of each loop iteration, right before the next `condition` check and is used to increment or decrement our loop counter.

Example:

```js
var ourArray = [];

for (var i = 0; i < 5; i++) {
  ourArray.push(i);
}
```

In the above example, we initialize the loop with `i = 0` and keep iterating while our condition `i < 5` is `true`. Then, as our `final-expression`, we increment `i` by `1` in each loop iteration with the `i++` syntax.
