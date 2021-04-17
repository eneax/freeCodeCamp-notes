# Comparison with the Strict Inequality Operator

The strict inequality operator (`!==`) is the opposite of the strict equality operator.
It means 'Strictly Not Equal' and it returns `false` in the cases where the strict equality operator would return `true`.

Moreover, just like the strict equality operator, the inequality operator doesn't perform a `type conversion` while comparing.

Examples:

```js
1 !== 2; // true
1 !== "1"; // true
1 !== true; // true
```
