# Render a Class Component to the DOM

None of the React code you write will render to the DOM without making a call to the `ReactDOM API`.
Its syntax consists of specifying as first argument the React component that you want to render and as second argument the DOM node that you want to render that component within: `ReactDOM.render(componentToRender, targetNode)`.

For React components, we need to use the same syntax as if you were rendering a nested component:
`ReactDOM.render(<ComponentToRender />, targetNode)`. 
We use this syntax for both ES6 class components and functional components.

```jsx
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
};

ReactDOM.render(<TypesOfFood />, document.getElementById('challenge-node'));
```
