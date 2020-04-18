# Use a Ternary Expression for Conditional Rendering

The ternary operator is probably the most used technique for conditional rendering among React developers.
Ternary expressions solve the main drawback of `if/else` statements: implementing conditional logic within JSX code. Since `if/else` statements can't be inserted directly into JSX, we have to write them always outside the `return` statement. A ternary operator, in contrast, doesn't have this problem.

In more details, ternary expression have three parts as we can see from this basic syntax:

```js
condition ? expressionIfTrue : expressionIfFalse;
```

The example below, instead, illustrates a more complex scenario where we can also nest ternary expressions:

```jsx
const inputStyle = {
  width: 235,
  margin: 5
};

class CheckUserAge extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      input: "",
      userAge: ""
    };

    this.submit = this.submit.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }

  handleChange(e) {
    this.setState({
      input: e.target.value,
      userAge: ""
    });
  }

  submit() {
    this.setState(state => ({
      userAge: state.input
    }));
  }

  render() {
    const buttonOne = <button onClick={this.submit}>Submit</button>;
    const buttonTwo = <button>You May Enter</button>;
    const buttonThree = <button>You Shall Not Pass</button>;
    const userAge = this.state.userAge;

    return (
      <div>
        <h3>Enter Your Age to Continue</h3>
        <input
          style={inputStyle}
          type="number"
          value={this.state.input}
          onChange={this.handleChange}
        />
        <br />
        {userAge === "" ? buttonOne : userAge < 18 ? buttonThree : buttonTwo}
      </div>
    );
  }
}
```
