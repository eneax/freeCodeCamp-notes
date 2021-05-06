# Add New Properties to a JavaScript Object

We can add new properties to existing JavaScript objects the same way we modify them.

Example:

```js
var player = {
  name: "Ronaldo"
};
console.log(player); // Ronaldo

player.number = 7;
player["goldenBalls"] = 5;
console.log(player); // {name: "Ronaldo", number: 7, goldenBalls: 5}
```
