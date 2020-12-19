# Use CSS Animation to Change the Hover State of a Button

You can use CSS `@keyframes` to change the color of a button in its hover state.

```html
<style>
  button {
    border-radius: 5px;
    color: white;
    background-color: #0f5897;
    padding: 5px 10px 8px 10px;
  }
  button:hover {
    animation-name: background-color;
    animation-duration: 500ms;
  }
  @keyframes background-color {
    100% {
      background-color: #4791d0;
    }
  }
</style>

<button>Register</button>
```
