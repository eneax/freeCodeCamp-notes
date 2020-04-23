# Get State from the Redux Store

Once we create a Redux `store` object, it provides us several methods that we can use to interact with it.

For instance, you can access the current state of our app held in the Redux store object with the `getState()` method:

```js
const store = Redux.createStore((state = 5) => state);

const currentState = store.getState();
```
