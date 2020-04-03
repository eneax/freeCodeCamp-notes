# Create a React Component

Another way to define a React component is with the ES6 `class` syntax.

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  
  render() {
    return (
      <div>
        <h1>Hello React!</h1>
      </div>
    )
  }
};
```

In the example above, `MyComponent` extends `React.Component` class.
It means that `MyComponent` class has now access to React features, such as lifecycle hooks. 
`MyComponent` class has also a `constructor` defined within it that calls `super()`.

Here, `super()` is used to call the constructor of the parent class, in this case `React.Component`.
The constructor is a special method used during the initialization of objects that are created with the class keyword. It is best practice to call a component's constructor with super, and pass props to both of them.
This makes sure the component is initialized properly.