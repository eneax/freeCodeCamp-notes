# Create a Controlled Form

React can control the internal state for different types of elements: from `input` and `textarea` to entire `form`.

```jsx
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      submit: ''
    };

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }

  handleSubmit(event) {
    event.preventDefault()
    this.setState((state) => ({
      submit: state.input
    }))
  }

  render() {
    return (
      <div>
        <form onSubmit={this.handleSubmit}>
          <input type='text' value={this.state.input} onChange={this.handleChange} />
          <button type='submit'>Submit!</button>
        </form>

        <h1>{this.state.submit}</h1>
      </div>
    );
  }
};
```

The state of `MyForm` component initializes with `input` and `submit` properties, both set to empty strings.

Typing in the `<input />` element updates the `input` property of the component's state, thanks to `handleChange()` method.

The `handleSubmit` method sets the component state property `submit` to the current `input` value in the local state.

Inside `handleSubmit`, we must call `event.preventDefault()` in order to prevent the default form submit behavior which will refresh the whole web page.

Finally, the `<h1>` header renders the value of the `submit` field from the component's state.
