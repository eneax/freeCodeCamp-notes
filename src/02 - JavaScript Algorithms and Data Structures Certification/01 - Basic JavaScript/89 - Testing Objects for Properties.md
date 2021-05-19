# Testing Objects for Properties

Sometimes it is useful to check if the property of a given object exists or not.
That's why we use the `.hasOwnProperty(propname)` object method to determine if that object has the given property name.
The `.hasOwnProperty()` method returns `true` or `false` if the property is found or not.

Example:

```js
function checkObj(obj, checkProp) {
  if (obj.hasOwnProperty(checkProp)) {
    return obj[checkProp];
  } else {
    return "Not Found";
  }
}
```
