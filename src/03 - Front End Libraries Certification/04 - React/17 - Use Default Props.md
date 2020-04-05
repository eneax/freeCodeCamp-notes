# Use Default Props

In React, we can assign default props to a component as a property on the component itself and React assigns the default prop if necessary. This allows us to specify what a prop value should be if no value is explicitly provided. 

React assigns default props if props are `undefined`, but if you pass `null` as the value for a prop, it will remain `null`.

```jsx
const MyComponent = (props) => {
  return (
    <div>
      <h1>Location: {props.location}</h1>
    </div>
  )
};

MyComponent.defaultProps = {
  location: 'Berlin'
}
```

In the example above, we've defined a `location` prop that's set to the string `'Berlin'` unless we specify otherwise.
