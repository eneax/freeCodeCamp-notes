# Optimize Re-Renders with shouldComponentUpdate

We've learnt so far that any time a React component receives new state or new props, it re-renders itself and all its children.
However, React gives us also the possibility to specify if a component should update or not.
This functionality is done thanks to the `shouldComponentUpdate()` method, which can be called when child components receive new state or props and it takes `nextProps` and `nextState` as parameters.

This lifecycle method is very useful for optimizing performance. In React, by default, a component re-renders anytime it receives new props, even if the props haven't changed.

Thus, we can use `shouldComponentUpdate()` to compare the `props` and prevent this behavior.
More specifically, we can compare the current props (`this.props`) to the next props (`nextProps`) to determine if we need to update or not, and return a `boolean` value that lets React know whether or not to update the component.

The code block below shows how we let the components to re-render only if the props that are being passed are even:

```jsx
class OnlyEvens extends React.Component {
  constructor(props) {
    super(props);
  }
  shouldComponentUpdate(nextProps, nextState) {
    console.log("Should I update?");

    if (this.props !== nextProps.value && nextProps.value % 2 === 0) {
      return true;
    }
  }
  componentDidUpdate() {
    console.log("Component re-rendered.");
  }
  render() {
    return <h1>{this.props.value}</h1>;
  }
}

class Controller extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: 0
    };
    this.addValue = this.addValue.bind(this);
  }
  addValue() {
    this.setState({
      value: this.state.value + 1
    });
  }
  render() {
    return (
      <div>
        <button onClick={this.addValue}>Add</button>
        <OnlyEvens value={this.state.value} />
      </div>
    );
  }
}
```

Here, first we compare the current props with the future props received by the `OnlyEvens` component and then check if the props are even. If so, we return `true` and the component re-renders.
