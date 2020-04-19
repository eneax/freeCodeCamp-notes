# Use Array.map() to Dynamically Render Elements

Conditional rendering is very useful when you know exactly what elements you want to render.
But if we need to render an unknown number of elements, then using `Array.map()` makes more sense.

For instance, if we create a simple "To Do" app, we can't know how many items the user might have on the list. For this reason, we need our component to be able to dynamically render the correct number of list elements.

```jsx
const textAreaStyles = {
  width: 235,
  margin: 5
};

class MyToDoList extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      userInput: "",
      toDoList: []
    };

    this.handleSubmit = this.handleSubmit.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }

  handleSubmit() {
    const itemsArray = this.state.userInput.split(",");
    this.setState({
      toDoList: itemsArray
    });
  }

  handleChange(e) {
    this.setState({
      userInput: e.target.value
    });
  }

  render() {
    const toDoList = this.state.toDoList;
    const items = toDoList.map(item => <li>{item}</li>);

    return (
      <div>
        <textarea
          onChange={this.handleChange}
          value={this.state.userInput}
          style={textAreaStyles}
          placeholder="Separate Items With Commas"
        />
        <br />
        <button onClick={this.handleSubmit}>Create List</button>
        <h1>My "To Do" List:</h1>
        <ul>{items}</ul>
      </div>
    );
  }
}
```

In the `MyToDoList` component above, we can see that when the `Create List` button is clicked, every item of a comma-separated list entered into the textarea element is transformed into an unordered list that contains each list item element and dynamically rendered on the screen.
