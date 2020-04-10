# Bind 'this' to a Class Method

The `this` keyword is one of the most confusing aspects of JavaScript but it plays an important role in React.

In React, we can define custom methods for our component class.
In order to allow custom methods to access the properties on the class (`state` and `props`) inside the scope of the method, we need to use the `this` keyword.

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      text: "Hello World!"
    };
    
    this.handleClick = this.handleClick.bind(this)
  }
  handleClick() {
    this.setState({
      text: "Clicked!"
    });
  }
  render() {
    return (
      <div>
        <button onClick={this.handleClick}>Click Me</button>
        <h1>{this.state.text}</h1>
      </div>
    );
  }
};
```

The `this` keyword is one of the most confusing aspects of JavaScript, but as we can see from the code above,
it can be used to explicitly bind `this` in the constructor so that `this` is bound to the class methods when the component is initialized.

Basically, when `this.setState()` is called within the class method, `this` will refer to the class itself and it will not be `undefined`.
