# Prioritize One Style Over Another

Sometimes your HTML elements will receive multiple styles that conflict with one another.
For example, your `h1` element can't be both green and pink at the same time.

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
</style>

<h1 class="pink-text">Hello World!</h1>
```

Our "pink-text" class will override our body element's CSS declaration!
