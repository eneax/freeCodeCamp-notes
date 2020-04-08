# Create a Stateful Component

State consists of any data our application needs to know about, that can change over time.
We want our apps to respond (or react) to state changes and present (or render) an updated UI when necessary. If the data changes, our UI will change accordingly.

React uses a `virtual DOM`, to keep track of changes behind the scenes. When state data updates, it triggers a re-render of the components using that data. React updates the actual DOM, but only where necessary. 

We simply declare what the UI should look like, without having to worry about changing the DOM.

We create state in a React component by declaring a state property on the component's `constructor`.
This initializes the component with state when it is created. The state property must be set to a JavaScript object:

```jsx
this.state = {
  // describe your state here
}
```

We'll have access to the state object throughout the life of the component. 
We can update the state, render it in our UI, and pass it as props to child components. 

```jsx
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    
    // initialize state here
    this.state = {
      name: 'Enea'
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
