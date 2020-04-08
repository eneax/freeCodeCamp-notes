# Render State in the User Interface

Once we've define a component's initial state, we can display any part of it in the UI. 
If a component is stateful, it will always have access to the data in state in its `render()` method. 

The way we access the data is with `this.state` and if we want to access the `state` value within the `return` of the `render` method, we have to wrap the value in `curly braces`. In JSX, any code we write with curly braces `{ }` will be treated as JavaScript.


```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      name: 'freeCodeCamp'
    }
  }

  render() {
    return (
      <div>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};
```

The example above represents a stateful component. Its state is completely encapsulated or local to that component; so no other components are aware of its state, unless we pass state data to a child component as props.
