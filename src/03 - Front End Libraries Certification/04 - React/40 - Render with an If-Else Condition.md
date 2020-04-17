# Render with an If-Else Condition

JavaScript is used in React also to control that the `render()` method renders the view that matches a particular condition that we've specified. That's how we can render different views according to the condition value `true` or `false`.

We can define a condition with the standard if/else statement:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      display: true
    };
    this.toggleDisplay = this.toggleDisplay.bind(this);
  }
  toggleDisplay() {
    this.setState({
      display: !this.state.display
    });
  }
  render() {
    const display = this.state.display;

    if (display) {
      return (
        <div>
          <button onClick={this.toggleDisplay}>Toggle Display</button>
          <h1>Displayed!</h1>
        </div>
      );
    } else {
      return (
        <div>
          <button onClick={this.toggleDisplay}>Toggle Display</button>
        </div>
      );
    }
  }
}
```
