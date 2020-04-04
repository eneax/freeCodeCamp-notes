# Write a React Component from Scratch

Always keep in mind that: 
- React components are the core building blocks of React applications
- a typical React component is an ES6 `class` which extends React.Component
- it has a `render()` method that returns HTML (from JSX) or null

```jsx
// change code below this line
class MyComponent extends React.Component {
  constructor(props) {
    super(props)
  }

  render() {
    return (
      <div>
        <h1>My First React Component!</h1>
      </div>
    )
  }
}

ReactDOM.render(<MyComponent/>, document.getElementById('challenge-node'))
```
