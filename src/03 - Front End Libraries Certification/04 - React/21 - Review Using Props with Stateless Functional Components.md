# Review Using Props with Stateless Functional Components

Before diving into the `state` topic, let's clarify some terminology.

### Stateless Functional Components
Stateless Functional Components are called also `pure functions`.
They accept props as input and return as output the same view every time they are passed the same props. 
Basically, a stateless functional component accepts props and returns JSX. 

### Stateless component
It's a `class` that extends `React.Component`, but does not use internal state.

### Stateful component
Stateful component, or React component or known simply as component, is a `class` component that does maintain its own internal state.

### Common Practice
It's common in React to try to minimize statefulness and to create stateless functional components wherever possible. 
This practice helps us confine the state to a specific area of your application, by improving the development and maintenance of our app and by making it easier to follow how changes to state affect its behavior.


```jsx
class Camper extends React.Component {
  constructor(props) {
    super(props)
  }

  render() {
    return (
      <p>{this.props.name}</p>
    )
  }
}

Camper.propTypes = {
  name: PropTypes.string.isRequired
}

Camper.defaultProps = {
  name: 'CamperBot' 
}

class CampSite extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <Camper/>
      </div>
    );
  }
};
```