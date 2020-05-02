# Use Provider to Connect Redux to React

Once we created a Redux store, which will be responsible for managing the state, we need to provide React access to the store. These task is handled by the `react-redux` package.

React Redux provides an API with two main features: `Provider` and `connect`.
The `Provider` is a wrapper component, that we import from the `react-redux` package, and it's used to wrap the entire React app, giving it access to the Redux `store`.

The `Provider` component takes two props, the Redux `store` and all the child components of our app:

```js
<Provider store={store}>
  <App />
</Provider>
```

The code block below illustrates a common approach of linking together React and Redux using `Provider`:

```js
// Redux Code:

// action type
const ADD = "ADD";

// action creator
const addMessage = message => {
  return {
    type: ADD,
    message
  };
};

// reducer
const messageReducer = (state = [], action) => {
  switch (action.type) {
    case ADD:
      return [...state, action.message];
    default:
      return state;
  }
};

const store = Redux.createStore(messageReducer);

// React Code:
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
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  submitMessage() {
    const currentMessage = this.state.input;
    this.setState({
      input: "",
      messages: this.state.messages.concat(currentMessage)
    });
  }
  render() {
    return (
      <div>
        <h2>Type in a new Message:</h2>
        <input value={this.state.input} onChange={this.handleChange} />
        <br />
        <button onClick={this.submitMessage}>Submit</button>
        <ul>
          {this.state.messages.map((message, idx) => {
            return <li key={idx}>{message}</li>;
          })}
        </ul>
      </div>
    );
  }
}

const Provider = ReactRedux.Provider;

class AppWrapper extends React.Component {
  render() {
    return (
      <Provider store={store}>
        <DisplayMessages />
      </Provider>
    );
  }
}
```
