# Set State with this.setState

Other than accessing the `state`, we can also modify it.
A key aspect of modifying `state` in React is that, we should not modify `state` directly, 
instead we should always use `this.setState()`.

Whenever changes occur, we should use the `setState` method for updating component state.
This method is called within your component class, by passing in an object with key-value pairs. 
The keys represent the state properties and the values are the updated state data. 

For instance, let's have a look at this example:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'Initial State'
    };
    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({
      name: "React 🤟🏻"
    })
  }
  render() {
    return (
      <div>
        <button onClick={this.handleClick}>Click Me</button>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};
```

As we can see in the example above, we were storing a `name` in state and want to update it when the button is clicked.
When the button element receives a click event in the browser, it triggers the `onClick()` handler. Then, the `handleClick()` method defined on `MyComponent` class runs and the `this.setState()` method sets the `name` property in state to equal the string `"React 🤟🏻"`.
