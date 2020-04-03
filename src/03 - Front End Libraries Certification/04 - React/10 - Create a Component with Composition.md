# Create a Component with Composition

To compose components together, you need to create a `parent component` which renders any other component as `children` components. 
To render a component as a child, we include the component name written as a custom HTML tag in the JSX:

```jsx
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>I'm the parent</h1>
        
        <ChildComponent />
      </div>
    );
  }
};
```
