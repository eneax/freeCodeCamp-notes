# Use Abbreviated Hex Code

For instance, red's hex code `#FF0000` can be shortened to `#F00`. This shortened form gives one digit for red, one digit for green, and one digit for blue. Browsers, however, will interpret `#FF0000` and `#F00` as exactly the same color.

Example:

```html
<style>
  .red-text {
    color: #f00;
  }
  .fuchsia-text {
    color: #f0f;
  }
  .cyan-text {
    color: #0ff;
  }
  .green-text {
    color: #0f0;
  }
</style>

<h1 class="red-text">I am red!</h1>

<h1 class="fuchsia-text">I am fuchsia!</h1>

<h1 class="cyan-text">I am cyan!</h1>

<h1 class="green-text">I am green!</h1>
```
