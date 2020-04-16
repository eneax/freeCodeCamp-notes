# Add Inline Styles in React

If you decide to use inline styles to style your React application, keep in mind that words which contain a hyphen (e.g. `font-size`) are invalid syntax for JavaScript object properties, so they must be written using camel case in JSX.

Moreover, unless otherwise specified, all length units are assumed to be in `px`. So, if you prefer to use `rem`, you need wrap the value and the units in quotes: like `{fontSize: "2rem"}`, instead of `{fontSize: 4}`.

```jsx
const customStyles = {
  color: "purple",
  fontSize: 40,
  border: "2px solid purple"
};

class Colorful extends React.Component {
  render() {
    return <div style={customStyles}>Style Content 🚀</div>;
  }
}
```
