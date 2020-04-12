# Pass State as Props to Child Components

In React, a common approach is to have a stateful component, containing the state which is important to your app, which then renders the child components.

We want these child components to have access only to some pieces of the entire state, which are passed in as props.

For instance, let's take into consideration an `App` component (parent component) that renders a Navbar and several other components.
Therefore, in our `App`, the `state` will contain a lot of information. The `Navbar`, however, only needs access to the user's username so it can display it. That's why we pass only that piece of state to the `Navbar` component as a prop.

From the example below, we can understand an important paradigm in React: `unidirectional data flow`.
It means that `state` flows in one direction: from top to bottom, from the the stateful parent component to child components. The child components only receive the piece of data (state) they need.

```jsx
class MyApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'Enea'
    }
  }

  render() {
    return (
       <div>
         <Navbar name={this.state.name} />
       </div>
    );
  }
};

class Navbar extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>Hello, my name is: {this.props.name}</h1>
      </div>
    );
  }
};
```

This code block illustrates also a React key principle: separation of state logic from UI logic.
React makes it easier to manage complex applications by allowing us to create even just a single stateful component, that handles any complex logic, and other presentational components that receive state from the parent as props, and render a UI from that state.
