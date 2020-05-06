# Understanding Uninitialized Variables

When working with variables, it's important to keep in mind that, when JavaScript variables are declared, they have an initial value of `undefined`.

For this reason, if we try to perform any mathematical operation with an `undefined` variable, we will get as a result `NaN` ("Not a Number").

```js
var a = 5;
var b = 10;
var c = "I am a";

a = a + 1;
b = b + 5;
c = c + " String!";

console.log(a); // 6
console.log(b); // 15
console.log(c); // "I am a String!"
```
