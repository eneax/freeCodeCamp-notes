# Override Class Declarations by Styling ID Attributes

We just proved that browsers read CSS from top to bottom in order of their declaration.
That means that, in the event of a conflict, the browser will use whichever CSS declaration came last.
Notice that if we even had put `blue-text` before `pink-text` in our `h1` element's classes, it would still look at the **declaration order** and not the order of their use!

There are other ways that you can override CSS: using id attributes!

Example:

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
  #orange-text {
    color: orange;
  }
</style>

<h1 class="pink-text blue-text" id="orange-text">Hello World!</h1>
```

**Note**: It doesn't matter whether you declare this `id` CSS styles, above or below pink-text class, since `id` attribute will always take precedence.
