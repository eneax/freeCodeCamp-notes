# Use PropTypes to Define the Props You Expect

React provides useful type-checking features to help us verify that components receive the correct type of props.

For instance, let's take the case of an application that makes an API call to retrieve data that we expect to be in an array, which is then passed to a component as a prop. 
We can set `propTypes` on our component to require the data to be of type `array`. If the data is of any other type, we'll get a useful warning on the console.

We can define a `propTypes` property for a component in the same way we define `defaultProps`. 

```jsx
import React from 'react'
import PropTypes from 'prop-types'

const Items = (props) => {
  return <h1>Items in Cart: {props.quantity}</h1>
}

Items.propsTypes = {
  quantity: PropTypes.number.isRequired
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

In the example above, the `PropTypes.number` checks that `quantity` is a `number`. 
Adding `isRequired` lets React know that `quantity` is a required property for that component. 
If that prop isn't provided, we will see a warning on the console. 

Among the seven JavaScript primitive types, function (written as `func`) and boolean (written as `bool`) are the only two `propTypes` that use unusual spelling. 

In addition to the primitive types, there are other types available; so make sure to check out the official [documentation](https://reactjs.org/docs/jsx-in-depth.html#specifying-the-react-element-type) for all of the options.
