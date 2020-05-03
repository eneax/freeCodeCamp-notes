# Map State to Props

The `Provider` wrapper component gives us access to `state` and `dispatch`, but we need to specify exactly what state we need for our React components.

This approach, of giving each component access only to the state it needs, is accomplished by using two functions: `mapStateToProps()` and `mapDispatchToProps()`.

The `mapStateToProps()` function takes `state` as argument and returns an `object` which maps that state to specific property names, that will be accessible to our component via `props`.

```js
const state = [];

const mapStateToProps = state => {
  return {
    messages: state
  };
};
```

In the example above, we pass an array as `state` to `mapStateToProps()` and return this array assigned to a `messages` key. Basically, it returns only the piece of state that interests a particular component.

Note: Behind the scenes, react-redux is using Redux's `store.subscribe()` method to implement `mapStateToProps()`.
