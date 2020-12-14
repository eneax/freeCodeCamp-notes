# Use a CSS Linear Gradient to Create a Striped Element

The `repeating-linear-gradient()` function is very similar to `linear-gradient()` with the major difference that it repeats the specified gradient pattern.
`repeating-linear-gradient()` accepts a variety of values, but for simplicity, we are going to work with an **angle value** and **color stop values**.

The **angle value** is the direction of the gradient. **Color stops** are like width values that mark where a transition takes place, and are given with a percentage or a number of pixels.

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50 auto;
    background: repeating-linear-gradient(
      90deg,
      yellow 0px,
      blue 40px,
      green 40px,
      red 80px
    );
  }
</style>

<div></div>
```

In the example above, the gradient starts with the color `yellow` at `0 pixels` which blends into the second color `blue` at `40 pixels` away from the start.
Since the next color stop is also at `40 pixels`, the gradient immediately changes to the third color `green`, which itself blends into the fourth color value `red` as that is `80 pixels` away from the beginning of the gradient.

For this example, it helps to think about the color stops as pairs where every two colors blend together:
`0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px`

If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50 auto;
    background: repeating-linear-gradient(
      45deg,
      yellow 0px,
      yellow 40px,
      black 40px,
      black 80px
    );
  }
</style>

<div></div>
```
