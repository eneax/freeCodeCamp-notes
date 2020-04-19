# Change Inline CSS Conditionally Based on Component State

We not only render components with conditional rendering, but also CSS styles.
We simply check if a condition is met and modify the styles object assigned to the JSX elements accordingly.

```jsx
class GateKeeper extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ""
    };
    this.handleChange = this.handleChange.bind(this);
  }
  handleChange(event) {
    this.setState({ input: event.target.value });
  }
  render() {
    let inputStyle = {
      border: "1px solid black"
    };

    if (this.state.input.length > 15) {
      inputStyle = {
        border: "3px solid red"
      };
    }

    return (
      <div>
        <h3>Don't Type Too Much:</h3>
        <input
          type="text"
          style={inputStyle}
          value={this.state.input}
          onChange={this.handleChange}
        />
      </div>
    );
  }
}
```

In this example, we style the input border red if the user types more than 15 characters of text in the input box.
