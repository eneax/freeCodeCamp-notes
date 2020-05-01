# Manage State Locally First

Once we created a stateful React component with an initial state, we can continue to work on the same component,
by completing its `render()` method:

```js
class DisplayMessages extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: "",
      messages: []
    };

    this.handleChange = this.handleChange.bind(this);
    this.submitMessage = this.submitMessage.bind(this);
  }

  handleChange(e) {
    e.preventDefault();
    this.setState({
      input: e.target.value
    });
  }

  submitMessage() {
    const { input, messages } = this.state;
    this.setState({
      // messages: messages.concat(input),
      messages: [...messages, input],
      input: ""
    });
  }

  render() {
    return (
      <div>
        <h2>Type in a new Message:</h2>

        <input value={this.state.input} onChange={this.handleChange} />
        <button onClick={this.submitMessage}>Add message</button>

        <ul>
          {this.state.messages.map(message => (
            <li key={message}>{message}</li>
          ))}
        </ul>
      </div>
    );
  }
}
```

The `DisplayMessages` stateful component renders the following tags: <h2>, <input>, <button>, <ul>.
The <input> element triggers the `handleChange()` method anytime it changes. This method updates the `input state` with what the user is typing.
The <button> element triggers the `submitMessage()` method when it's clicked. This methods takes the message stored in the `input state` and adds it to the `messages` array in the local state. Then it clears the value of the <input>.

Finally, we `map()` over the `messages` array and render <li> elements to the screen as a list.
