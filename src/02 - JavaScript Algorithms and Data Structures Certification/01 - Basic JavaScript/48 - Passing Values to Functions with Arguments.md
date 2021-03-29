# Passing Values to Functions with Arguments

When we create a function, we usually define it along with one or more `parameters`.
A `parameter` is a variable that behaves like a `placeholder` for the values that we'll input to the function when it's called.
`Arguments`, instead are the `actual values` that we pass as input into a function when it's called.

```js
function addNumbers(number1, number2) {
  console.log(number1 + number2);
}

addNumbers(1, 2); // 3
```
