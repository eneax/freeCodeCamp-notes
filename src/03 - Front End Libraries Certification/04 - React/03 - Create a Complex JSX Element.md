# Create a Complex JSX Element

Keep in mind that JSX must return a single element.
This one parent element would wrap all of the other levels of nested elements.

```jsx
<div>
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
  <p>Paragraph 3</p>
</div>
```

and 

```jsx
const JSX = (
  <div>
    <h1>This is a title</h1>
    <p>This is a subtitle</p>
  </div>
);
```