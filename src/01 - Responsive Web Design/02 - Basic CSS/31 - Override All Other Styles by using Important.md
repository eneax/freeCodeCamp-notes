# Override All Other Styles by using Important

We just proved that **inline styles** will override _all_ the CSS declarations in your style element. However, there's one last way to override CSS, the most powerful method of all, `!important`.

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
    color: pink !important;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white">
  Hello World!
</h1>
```
