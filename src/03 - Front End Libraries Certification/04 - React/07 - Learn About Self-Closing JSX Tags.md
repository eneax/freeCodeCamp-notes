# Learn About Self-Closing JSX Tags

Another important way in which JSX differs from HTML is in self-closing tags.

Any JSX element can be written with a self-closing tag, and every element must be closed. 
For instance, the line-break tag must always be written as <br /> in order to be valid JSX that can be transpiled. A <div>, instead, can be written as <div /> or <div></div>. 
The difference is that in the first syntax version there is no way to include anything in the <div />. 

```jsx
const jsxVariable = (
  <div>
    <h2>Welcome to React!</h2> <br />
    <p>Be sure to close all tags!</p>
    <hr />
  </div>
);
```