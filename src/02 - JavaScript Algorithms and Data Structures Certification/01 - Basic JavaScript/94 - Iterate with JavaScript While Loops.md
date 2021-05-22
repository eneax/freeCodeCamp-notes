# Iterate with JavaScript While Loops

In programming, we can run the same code multiple times by using a `loop`.
In JavaScript, we have different types of loops, and the first one we'll examine is the `while loop`.
It's called while loop because it runs "while" a particular condition is `true` and stops once that condition becomes `false`.

Example:

```js
var myArray = [];

var i = 0;
while (i < 5) {
  myArray.push(i);
  i++;
}

console.log(myArray); // [0, 1, 2, 3, 4]
```
