# Use the Lifecycle Method componentWillMount

React allows us to intervene at a specific point in the lifecycle of a component, in order to perform particular action.
We've this opportunity thanks to several special methods, also known as lifecycle methods or lifecycle hooks.
Here is a list of some of the main lifecycle methods: `componentWillMount()`, `shouldComponentUpdate()`, `componentDidUpdate()`, `componentWillUnmount()`.

Below we can see a simple example of a React component containing `componentWillMount()` lifecycle method:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  componentWillMount() {
    console.log("Testing componentWillMount");
  }
  render() {
    return <div />;
  }
}
```

The `componentWillMount()` method is called before the `render()` method when a component is being mounted to the DOM.

[Note](https://reactjs.org/blog/2018/03/27/update-on-async-rendering.html): The componentWillMount Lifecycle method will be deprecated in a future version of `16.X` and removed in version `17`.
