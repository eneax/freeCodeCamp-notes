# Use the CSS Transform Property skewX to Skew an Element Along the X-Axis

Another function of the `transform` property is `skewX()`, which skews the selected element along its X (**horizontal**) axis by a given degree.

Example:

```html
<style>
  div {
    width: 70%;
    height: 100px;
    margin: 50px auto;
  }
  #top {
    background-color: red;
  }
  #bottom {
    background-color: blue;
    transform: skewX(24deg);
  }
</style>

<div id="top"></div>
<div id="bottom"></div>
```
