# Using Objects for Lookups

When we know that our input data is limited to a certain range, we can use an object to look for values rather than a `switch` statement or an `if/else` chain.

Example:

```js
// Setup
function phoneticLookup(val) {
  var result = "";

  var lookup = {
    alpha: "Adams",
    bravo: "Boston",
    charlie: "Chicago",
    delta: "Denver",
    echo: "Easy",
    foxtrot: "Frank"
  };

  result = lookup[val];
  return result;
}

phoneticLookup("charlie");
```
