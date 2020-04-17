# Use && for a More Concise Conditional

The if/else statements are a great way to render different views based on a specific condition, but we can achieve the same result with a more elegant syntax.

Instead of repeating code and increasing the probability to make mistakes, we can use the `&&` logical operator to perform conditional logic in a simpler way.

It allows us to to check if a condition is `true`, and in that case returns a specific view:

```jsx
{
  condition && <p>Just a paragraph</p>;
}
```

If the condition is not matched, the operation will immediately return `false` and no view will be rendered.

The code block below, gives a better representation of the `&&` logical operator in action:

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
    this.setState(state => ({
      display: !state.display
    }));
  }
  render() {
    const display = this.state.display;

    return (
      <div>
        <button onClick={this.toggleDisplay}>Toggle Display</button>
        {display && <h1>Displayed!</h1>}
      </div>
    );
  }
}
```
