# Iterate with JavaScript Do...While Loops

Another type of loop in JavaScript is the `do...while loop`.
The reason behind this name is related to the fact that it will first execute the code inside the loop no matter what, and then, it'll continue to run the loop only while the specified condition evaluates to `true`.

```js
var myArray = [];
var i = 10;

do {
  myArray.push(i);
  i++;
} while (i < 5);

console.log(i); // 11
```

The `do...while loop` is very similar to the `while loop`.
The main difference is that in the `do...while loop`, the code inside the loop will run at least once.
In the `while loop` instead, the code doesn't run if the initial condition is `false`.
