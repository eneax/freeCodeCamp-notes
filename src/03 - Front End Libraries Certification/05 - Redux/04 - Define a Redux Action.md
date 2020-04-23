# Define a Redux Action

In Redux, the only way we have to update state is to dispatch actions.
An `action` is a JavaScript object that contains information about an event that has occurred in our application.
Then, our Redux store will receive these action objects and update the state accordingly.

A Redux action is made of a `type` property, which specifies the type of of action that occurred, and a `payload`, which carries some data. While the `type` property is required, the `payload` is optional.

```js
const action = {
  type: "LOGIN"
};
```
