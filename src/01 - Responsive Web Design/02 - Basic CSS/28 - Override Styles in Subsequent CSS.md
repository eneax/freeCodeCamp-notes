# Override Styles in Subsequent CSS

Classes will override the body element's CSS.
So the next logical question is, what can we do to override our pink-text class?

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
</style>

<h1 class="pink-text blue-text">Hello World!</h1>
```

The order of the class declarations in the `<style>` section is what is important.
The second declaration will always take precedence over the first. Because `.blue-text` is declared second, it overrides the attributes of `.pink-text`.
