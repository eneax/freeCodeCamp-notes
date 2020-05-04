# Connect Redux to the Messages App

When working with `react-redux`, it's important to distinguish between two types of components: `presentational` and `container` components.

A `presentational` component is not directly connected to Redux. It cares only about receiving `props` and returning a UI.
A `container` component, on the other hand, is directly connected to Redux. This type of component deals with tasks like: passing the `store state` to child components as `props` and `dispatching actions` to the `store`.

The example below, illustrates both `presentational` and `container` components in action:

```jsx
// Redux:

// action type
const ADD = "ADD";

// action creator
const addMessage = message => {
  return {
    type: ADD,
    message: message
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

// React:
class Presentational extends React.Component {
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

// React-Redux:
const mapStateToProps = state => {
  return { messages: state };
};

const mapDispatchToProps = dispatch => {
  return {
    submitNewMessage: newMessage => {
      dispatch(addMessage(newMessage));
    }
  };
};

const Provider = ReactRedux.Provider;
const connect = ReactRedux.connect;

// connected component
const Container = connect(mapStateToProps, mapDispatchToProps)(Presentational);

class AppWrapper extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <Container store={store}>
        <Presentational />
      </Container>
    );
  }
}
```
