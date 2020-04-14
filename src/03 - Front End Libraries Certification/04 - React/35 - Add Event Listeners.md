# Add Event Listeners

The `componentDidMount()` lifecycle method is also used to attach any event listeners we need to add in order to build a specific functionality.

We have already seen how to work with event handlers, such as `onClick()`.
However, if we want to attach an event handler to the `document` or `window` objects, we have to do this directly.

The code block below illustrates how to add a `keydown` event handler in React:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: ""
    };

    this.handleEnter = this.handleEnter.bind(this);
    this.handleKeyPress = this.handleKeyPress.bind(this);
  }

  componentDidMount() {
    document.addEventListener("keydown", this.handleKeyPress);
  }
  componentWillUnmount() {
    document.removeEventListener("keydown", this.handleKeyPress);
  }

  handleEnter() {
    this.setState({
      message: this.state.message + "You pressed the enter key! "
    });
  }

  handleKeyPress(event) {
    if (event.keyCode === 13) {
      this.handleEnter();
    }
  }

  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
      </div>
    );
  }
}
```
