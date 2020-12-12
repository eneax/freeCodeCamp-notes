# Learn about Complementary Colors

On a website, color can draw attention to content, evoke emotions, or create visual harmony. Using different combinations of colors can really change the look of a website, and a lot of thought can go into picking a color palette that works with your content.

The color wheel is a useful tool to visualize how colors relate to each other - it's a circle where similar hues are neighbors and different hues are farther apart. When _two colors are opposite each other_ on the wheel, they are called **complementary colors**. They have the characteristic that if they are combined, they "cancel" each other out and create a gray color. However, when placed side-by-side, these colors appear more vibrant and produce a strong visual contrast.

Some examples of complementary colors with their hex codes are:

- red (`#FF0000`) and cyan (`#00FFFF`)
- green (`#00FF00`) and magenta (`#FF00FF`)
- blue (`#0000FF`) and yellow (`#FFFF00`)

Modern **color theory** uses the additive RGB model (like on a computer screen) and the subtractive CMY(K) model (like in printing). More info [here](https://en.wikipedia.org/wiki/Color_model).

Example:

```html
<style>
  body {
    background-color: #ffffff;
  }
  .blue {
    background-color: blue;
  }
  .yellow {
    background-color: yellow;
  }
  div {
    display: inline-block;
    height: 100px;
    width: 100px;
  }
</style>
<div class="blue"></div>
<div class="yellow"></div>
```
