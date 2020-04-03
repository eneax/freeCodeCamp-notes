# Create a Stateless Functional Component

Components are the core of React. In fact, everything in React is a component.

One way to create a React component is to use a JavaScript function; which in this case, will create a `stateless functional component`. A stateless component is a component that can receive data and render it, but does not manage or track changes to that data.

To create a component with a function, you simply write a JavaScript function that returns either `JSX` or `null`. 
One important thing to remember is that React requires your function name to begin with a `capital letter`:

```jsx
const MyComponent = function() {
  return (
    <div>This div element contains a string of text.</div>
  )
}
```
