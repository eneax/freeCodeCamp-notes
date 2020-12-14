# Create a Gradual CSS Linear Gradient

CSS provides the ability to use color transitions, or **gradients**, on elements.
This is accessed through the background property's `linear-gradient()` function. Here is the general syntax:

`background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);`

The first argument specifies the direction from which color transition starts - it can be stated as a degree, where `90deg` makes a horizontal gradient (from left to right) and `45deg` is angled like a backslash.

Example:

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;
    background: linear-gradient(35deg, #ccffff, #ffcccc);
  }
</style>

<div></div>
```
