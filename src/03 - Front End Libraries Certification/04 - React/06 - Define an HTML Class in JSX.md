# Define an HTML Class in JSX

HTML and JSX quite similar.
However, one important difference is that in JSX we can no longer use the word `class` to define HTML classes.
This is because `class` is a reserved word in JavaScript. Instead, JSX uses `className`.

In fact, all HTML attributes and event references in JSX become `camelCase`. 
For instance, a click event in JSX is `onClick`, instead of onclick and onchange becomes `onChange`.

```jsx
const JSX = (
  <div className='myDiv'>
    <h1>Add a class to this div</h1>
  </div>
);
```
