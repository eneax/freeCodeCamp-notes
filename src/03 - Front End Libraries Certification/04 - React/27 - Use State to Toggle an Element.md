# Use State to Toggle an Element

React state updates can be asynchronous. This means that React can batch together multiple `setState()` calls into a single update.
That's why we cannot rely on the previous value of `this.state` or `this.props` when calculating our next value. 

What we should do instead is pass `setState` a function that allows us to access state and props.
By using a function with `setState`, we are sure that we are working with the latest values of state and props. 

Here is an example where we pass `setState` a function that allows us to access both `state` and `props`: 

```jsx
this.setState((state, props) => ({
  counter: state.counter + props.increment
}));
```

In case `props` are not needed and only `state` is passed: 

```jsx
this.setState(state => ({
  counter: state.counter + 1
}));
```

Here is also an example of how to toggle an element in React:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      visibility: false
    };
    
    this.toggleVisibility = this.toggleVisibility.bind(this)
  }

  toggleVisibility() {
    this.setState((state) => ({
      visibility: !state.visibility
    }))
  }

  render() {
    if (this.state.visibility) {
      return (
        <div>
          <button onClick={this.toggleVisibility}>Click Me</button>
          <h1>Now you see me!</h1>
        </div>
      );
    } else {
      return (
        <div>
          <button onClick={this.toggleVisibility}>Click Me</button>
        </div>
      );
    }
  }
};
```

`MyComponent` has a `visibility` property initialized to `false`. 
The `render()` method returns one view if the value of `visibility` is `true`, and a different view if it is `false`.

There is a click handler on the button which triggers a class method called `toggleVisibility()`. 
It passes a function to `setState` to define this method so that the state of visibility toggles to the opposite value when the method is called. If visibility is `false`, the method sets it to `true`, and vice versa.
