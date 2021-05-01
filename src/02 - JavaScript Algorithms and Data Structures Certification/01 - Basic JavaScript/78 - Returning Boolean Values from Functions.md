# Returning Boolean Values from Functions

We can use an `if/else` statement to do a comparison, like this:

```js
function isLess(a, b) {
  if (a < b) {
    return true;
  } else {
    return false;
  }
}

isLess(10, 15);
```

However, since `comparison operators` return `true` or `false`, we can immediately return the result of the comparison, without the need to write an `if/else` statement:

```js
function isLess(a, b) {
  return a < b;
}

isLess(10, 15);
```
