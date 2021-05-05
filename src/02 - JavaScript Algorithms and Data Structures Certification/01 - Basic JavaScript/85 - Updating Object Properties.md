# Updating Object Properties

Once a JavaScript object has been created, we can update its properties at any time by using either `dot` or `bracket notation`.

Example:

```js
var player = {
  name: "Ronaldo",
  number: 7,
  goldenBalls: 5
};
console.log(player); // {name: "Ronaldo", number: 7, goldenBalls: 5}

player.name = "Del Piero";
player.number = 10;
console.log(player); // {name: "Del Piero", number: 10, goldenBalls: 5}
```
