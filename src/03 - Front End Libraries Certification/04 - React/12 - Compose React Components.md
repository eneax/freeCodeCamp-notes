# Compose React Components

Here is any example of how to you can render `JSX elements`, `stateless functional components`, and ES6 `class` components within other components: 

```jsx
const RandomVeggies = () => (
  <ul>
    <li>Brussel Sprouts</li>
    <li>Broccoli</li>
    <li>Squash</li>
  </ul>
);

const NonCitrusFruits = () => (
  <ul>
    <li>Apples</li>
    <li>Blueberries</li>
    <li>Strawberries</li>
    <li>Bananas</li>
  </ul>
);

const CitrusFruits = () => (
  <ul>
    <li>Lemon</li>
    <li>Lime</li>
    <li>Orange</li>
    <li>Grapefruit</li>
  </ul>
);

const NonCitrus = () => (
  <div>
    <h3>Non-Citrus:</h3>
    <NonCitrusFruits />
  </div>
);

const Citrus = () => (
  <div>
    <h3>Citrus:</h3>
    <CitrusFruits />
  </div>
);

class Fruits extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h2>Fruits:</h2>
        <NonCitrus />
        <Citrus />
      </div>
    );
  }
}

class Vegetables extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h2>Vegetables:</h2>
        <RandomVeggies />
      </div>
    );
  }
}

class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        <Fruits />
        <Vegetables />
      </div>
    );
  }
}
```
