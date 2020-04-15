# Introducing Inline Styles

A React application can be styled in several ways. A common approach is to use stylesheets and import styles from it. In this way, we can apply a class to our JSX element using the `className` attribute and add styles to the class in our stylesheet.

Another option can be to apply inline styles to a JSX element, similarly to how we do it in HTML, but with few JSX differences.

In HTML, we use the `style` attribute and pass a string to it:

```html
<div style="color: orange; font-size: 16px">Orange</div>
```

In JSX, we still use the `style` attribute, but we set it equal to a JavaScript object:

```jsx
<div style={{ color: "orange", fontSize: 18 }}>Orange</div>
```

or

```jsx
<div style={{ color: "orange", fontSize: "18px" }}>Orange</div>
```

It's important to notice how we camelCase the `fontSize` property, since React doesn't accept kebab-case keys in the style object. Moreover, we can set the font size to be a number, omitting the units "px", or write it as "18px".
