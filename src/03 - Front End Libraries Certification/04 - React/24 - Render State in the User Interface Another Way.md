# Render State in the User Interface Another Way

State can be accessed not only in the `return` statement, but also in the `render()` method, just before the `return`. 
In this area of the stateful component, we can declare functions, access data from state or props and perform computations on the data. Then, we can assign any data to variables, which can be accessed in the `return` statement.

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  render() {
    const name = this.state.name
    
    return (
      <div>
        <h1>{name}</h1>
      </div>
    );
  }
};
```
