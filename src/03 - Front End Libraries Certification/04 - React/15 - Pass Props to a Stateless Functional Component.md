# Pass Props to a Stateless Functional Component

Another key feature of React is `props`. In React, you can pass properties, or props, to child components. 
Say you have a `Calendar` component which renders a child component called `CurrentDate` which is a stateless functional component. You can pass `CurrentDate` a `date` property by writing:

```jsx
class Calendar extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h3>What date is it?</h3>

        <CurrentDate date={Date()} />
      </div>
    );
  }
};
```

We use custom HTML attributes to be passed to the component. 
The created property `date` is passed to the component `CurrentDate`. 
Since `CurrentDate` is a stateless functional component, it has access to this value like so:

```jsx
const CurrentDate = (props) => {
  return (
    <div>
      <p>The current date is: {props.date}</p>
    </div>
  );
};
```

When dealing with stateless functional components, it is common practice to to call this value `props`.
Basically, we consider it as an argument that is passed to a function which will return JSX.
Then, we can access the value of the argument in the function body. 
