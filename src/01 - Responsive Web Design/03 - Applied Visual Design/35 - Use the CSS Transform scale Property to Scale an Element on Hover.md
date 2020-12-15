# Use the CSS Transform scale Property to Scale an Element on Hover

The `transform` property has a variety of functions that let you `scale`, `move`, `rotate`, `skew`, etc., your elements. When used with pseudo-classes such as `:hover` that specify a certain state of an element, the `transform` property can easily add **interactivity** to your elements.

```html
<style>
  div {
    width: 70%;
    height: 100px;
    margin: 50px auto;
    background: linear-gradient(53deg, #ccfffc, #ffcccf);
  }

  div:hover {
    transform: scale(1.1);
  }
</style>

<div></div>
```

**Note**: Applying a transform to a div element will also affect any child elements contained in the div.
