# Use React to Render Nested Components

Component composition is one of most React's powerful features. 
That's why it's important to start thinking about your user interface in terms of components. 
You break down your UI into its basic building blocks, and those pieces become the components. 
This helps to separate the code responsible for the UI from the code responsible for handling your application logic. 
It can greatly simplify the development and maintenance of complex projects.

```jsx
const TypesOfFruit = () => {
  return (
    <div>
      <h2>Fruits:</h2>
      <ul>
        <li>Apples</li>
        <li>Blueberries</li>
        <li>Strawberries</li>
        <li>Bananas</li>
      </ul>
    </div>
  );
};

const Fruits = () => {
  return (
    <div>
      <TypesOfFruit />
    </div>
  );
};

class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        <Fruits />
      </div>
    );
  }
};
```
