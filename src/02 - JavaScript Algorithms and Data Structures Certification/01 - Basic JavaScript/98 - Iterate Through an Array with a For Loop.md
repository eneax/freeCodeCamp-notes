# Iterate Through an Array with a For Loop

In JavaScript is very common to to iterate through the contents of an array and perform some mathematical operation with each element of the array or display them on the screen.

In the example below, we loop over an array and add the value of each element of the `myArr` array to `total` variable.

```js
var myArr = [2, 3, 4, 5, 6];

var total = 0;
for (var i = 0; i < myArr.length; i++) {
  total += myArr[i];
}

console.log(total); // 20
```
