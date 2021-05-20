# Accessing Nested Objects

We can access sub-properties of objects by chaining together the `dot` or `bracket` notation.

Example:

```js
var myStorage = {
  car: {
    inside: {
      "glove box": "maps",
      "passenger seat": "crumbs"
    },
    outside: {
      trunk: "jack"
    }
  }
};

var gloveBoxContents = myStorage.car.inside["glove box"];
```
