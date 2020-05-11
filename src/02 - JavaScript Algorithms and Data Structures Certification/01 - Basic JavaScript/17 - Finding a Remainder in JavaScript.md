# Finding a Remainder in JavaScript

In programming, it's common to check if a number is `even` (divisible by 2) or `odd` (not divisible by 2).

The remainder operator `%` gives the remainder of the division of two numbers:

```js
17 % 2 = 1; // 17 ==> Odd
10 % 2 = 0; // 10 ==> Even
```

We can break this down by:

```js
Math.floor(17 / 2) = 8;
8 * 2 = 16;
17 - 16 = 1; // Remainder
```
