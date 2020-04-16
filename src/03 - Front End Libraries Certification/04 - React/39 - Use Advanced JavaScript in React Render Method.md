# Use Advanced JavaScript in React Render Method

So far we learnt that, in order to inject JavaScript code into React, we can simply use curly braces `{ }` and we can perform several tasks like accessing props, passing props, accessing state, inserting comments into our code, and also style our components.

However, if we don't want to insert JavaScript code inside curly braces, we can write it directly in the `render()` method.

```jsx
const inputStyle = {
  width: 235,
  margin: 5
};

class MagicEightBall extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      userInput: "",
      randomIndex: ""
    };

    this.ask = this.ask.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }

  ask() {
    if (this.state.userInput) {
      this.setState({
        randomIndex: Math.floor(Math.random() * 20),
        userInput: ""
      });
    }
  }

  handleChange(event) {
    this.setState({
      userInput: event.target.value
    });
  }

  render() {
    const possibleAnswers = [
      "It is certain",
      "It is decidedly so",
      "Without a doubt",
      "Yes, definitely",
      "You may rely on it",
      "As I see it, yes",
      "Outlook good",
      "Yes",
      "Signs point to yes",
      "Reply hazy try again",
      "Ask again later",
      "Better not tell you now",
      "Cannot predict now",
      "Concentrate and ask again",
      "Don't count on it",
      "My reply is no",
      "My sources say no",
      "Most likely",
      "Outlook not so good",
      "Very doubtful"
    ];

    const answer = this.state.randomIndex;

    return (
      <div>
        <input
          type="text"
          value={this.state.userInput}
          onChange={this.handleChange}
          style={inputStyle}
        />
        <br />
        <button onClick={this.ask}>Ask the Magic Eight Ball!</button>
        <br />
        <h3>Answer:</h3>
        <p>{possibleAnswers[answer]}</p>
      </div>
    );
  }
}
```

In this code block above, we can see the `onClick` event in the button calls the `ask()` method, which generates a random number that is stored in the state as `randomIndex`.

Here, the render method contains the `possibleAnswers` array to represent the answers found in the classic 1980's Magic Eight Ball toy and the `answer` variable which accesses the value of the `randomIndex` from `state`.
