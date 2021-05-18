# Delete Properties from a JavaScript Object

We can also delete properties from objects like this:

```js
var player = {
  name: "Ronaldo",
  number: 7,
  goldenBalls: 5
};
console.log(player); // {name: "Ronaldo", number: 7, goldenBalls: 5}

delete player.goldenBalls; // returns true if successful
console.log(player); // {name: "Ronaldo", number: 7}
```
