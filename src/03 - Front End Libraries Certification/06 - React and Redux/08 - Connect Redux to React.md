# Connect Redux to React

As we mentioned before, the easiest way to connect React with Redux is to use the `react-redux` package.
It provides an API with two main features: `Provider` and `connect`. We already examined the `Provider` wrapper component, so here we'll analyse the `connect` method.

This method takes two optional arguments, `mapStateToProps()` and `mapDispatchToProps()`:

```jsx
const MyConnectedComponent = connect(
  mapStateToProps,
  mapDispatchToProps
)(MyComponent);
```

However, if a component only needs access to the `state` and doesn't need to dispatch any actions, we can pass `null` in its place:

```js
const MyConnectedComponent = connect(mapStateToProps, null)(MyComponent);
```

The code below illustrates how to use `mapStateToProps()`, `mapDispatchToProps()` and `connect` in order to connect the React `Presentational` component with Redux:

```js
const addMessage = message => {
  return {
    type: "ADD",
    message: message
  };
};

const mapStateToProps = state => {
  return {
    messages: state
  };
};

const mapDispatchToProps = dispatch => {
  return {
    submitNewMessage: message => {
      dispatch(addMessage(message));
    }
  };
};

class Presentational extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <h3>This is a Presentational Component</h3>;
  }
}

const connect = ReactRedux.connect;

const ConnectedComponent = connect(
  mapStateToProps,
  mapDispatchToProps
)(Presentational);
```
