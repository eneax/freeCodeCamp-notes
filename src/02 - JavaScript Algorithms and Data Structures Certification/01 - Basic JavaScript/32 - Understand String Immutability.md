# Understand String Immutability

In JavaScript, `String` are `immutable`. This means that they cannot be modified once created.

For instance:

```js
var myStringVariable = "Jello World";

// First character will still be "J"
myStringVariable[0] = "H";

// Right way to mutate a string
myStringVariable = "Hello World";
```

As we can see from the code above, `String immutability` doesn't mean that the string variable cannot be changed, just that the single individual character of a `string literal` cannot be changed.

That's why the only way we can change `myStringVariable` is to assign it with a completely new string:

```js
myStringVariable = "Hello World";
```
