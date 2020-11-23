# Override Class Declarations with Inline Styles

So we've proven that `id` declarations override `class` declarations, regardless of where they are declared in your style element CSS.

There are other ways that you can override CSS: inline styles!

Example:

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  #orange-text {
    color: orange;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white;">
  Hello World!
</h1>
```
