# Pass an Array as Props

To pass an array to a JSX element, it must be treated as JavaScript and wrapped in curly braces.

```jsx
<ParentComponent>
  <ChildComponent team={["Ronaldo", "Dybala", "Higuain"]} />
</ParentComponent>
```

Then, the child component will have access to the array property `team`. 
Array methods such as `join()` can be used when accessing the property. 

```jsx
const ChildComponent = (props) => <p>{props.team.join(', ')}</p>
```

The above code will join all `team` array items into a comma separated string and produce: 
<p>Ronaldo, Dybala, Higuain</p>.
