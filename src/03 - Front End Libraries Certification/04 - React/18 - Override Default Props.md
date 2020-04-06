# Override Default Props

Once a default value has been specified, we can override it by explicitly setting the prop values for a component.

```jsx
const Items = (props) => {
  return <h1>Items in Cart: {props.quantity}</h1>
}

Items.defaultProps = {
  quantity: 0
}

class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return <Items quantity={10} />
  }
};
```

The `Items` component has a default prop quantity set to the integer `0`. 
The only way to override the default prop is by passing in an integer value for quantity.
