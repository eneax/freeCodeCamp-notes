# Give Sibling Elements a Unique Key Attribute

In order to dynamically render a number of elements we can use the `map()` method. However, every time we create an array of elements, each one of them needs a `key` attribute set to a unique value.

This unique value is used by React to keep track of which items are added, modified, or removed; so that React can handle the re-rendering process in a more efficient way.

In the example below, we can see the stateless functional component `Frameworks()` which loops over the `frontEndFrameworks` array and returns an unordered list, where each <li> has a key attribute set to a unique value.

```jsx
const frontEndFrameworks = [
  "React",
  "Angular",
  "Ember",
  "Knockout",
  "Backbone",
  "Vue"
];

function Frameworks() {
  const renderFrameworks = frontEndFrameworks.map(item => (
    <li key={item}>{item}</li>
  ));

  return (
    <div>
      <h1>Popular Front End JavaScript Frameworks</h1>
      <ul>{renderFrameworks}</ul>
    </div>
  );
}
```
