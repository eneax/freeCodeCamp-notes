# Use the Lifecycle Method componentDidMount

As web developers, we are used to make API calls. If your application is build with React, the action of calling an API endpoint in order to retrieve data is performed inside the `componentDidMount()` method.
This method is called only after a component is successfully mounted to the DOM.

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      activeUsers: null
    };
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({
        activeUsers: 12345
      });
    }, 500);
  }
  render() {
    return (
      <div>
        <h1>Active Users: {this.state.activeUsers}</h1>
      </div>
    );
  }
}
```

In the code block above, we're mocking an API call in `componentDidMount()`.
Any calls to `setState()` will trigger a re-rendering of `MyComponent`.
When we call an API in this method, and set the state with the data that the API returns, it will automatically trigger an update once the data is retrieved.
Then, the state is updated and the final result is displayed with an <h1> tag.
