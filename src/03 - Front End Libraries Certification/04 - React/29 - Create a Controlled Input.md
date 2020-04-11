# Create a Controlled Input

A controlled input form is a React component with input fields where the user can type into.
Form control elements for text input (e.g. input or textarea) maintain their own state in the DOM while the user types. 

In React, this mutable state can be moved into a React component's state. 
Thus, the user's input becomes part of the application state, allowing React to control the value of that input field. 

In the code block below, we can see an example of a controlled input element inside the `ControlledInput` component.

```jsx
class ControlledInput extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ''
    };

    this.handleChange = this.handleChange.bind(this)
  }

  handleChange(event) {
    this.setState({
      input: event.target.value
    })
  }

  render() {
    return (
      <div>
        <input type="text" value={this.state.input} onChange={this.handleChange} />

        <h4>Controlled Input:</h4>
        <p>{this.state.input}</p>
      </div>
    );
  }
};
```

Here, the component's `state` is already initialized with an `input` property that holds an empty string.
It represents the text a user typically types into the input field.

Once, the component has been initialized with the `constructor`, we create a method called `handleChange()` that takes a parameter called `event`.
When this method is called, it receives the event object that contains a string of text from the input element.
Then, we can access this string with `event.target.value` inside the method and use `this.setState()` to update the input property of the component's state.

Finally, in the render method, we display the result (what the user typed) thanks to the `value` attribute which is equal to the input property of the component's state.
