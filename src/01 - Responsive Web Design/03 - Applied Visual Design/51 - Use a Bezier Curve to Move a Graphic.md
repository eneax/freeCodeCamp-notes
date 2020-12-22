# Use a Bezier Curve to Move a Graphic

The `ease-out` keyword describes an animation change that speeds up first and then slows down at the end of the animation.
Similar animation progressions to the `ease-out` keyword can be achieved by using a custom cubic Bezier curve function: `animation-timing-function: cubic-bezier(0, 0, 0.58, 1);`.

Example:

```html
<style>
  .balls {
    border-radius: 50%;
    position: fixed;
    width: 50px;
    height: 50px;
    margin-top: 50px;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #red {
    background: red;
    left: 27%;
    animation-timing-function: cubic-bezier(0, 0, 0.58, 1);
  }
  #blue {
    background: blue;
    left: 56%;
    animation-timing-function: ease-out;
  }
  @keyframes bounce {
    0% {
      top: 0px;
    }
    100% {
      top: 249px;
    }
  }
</style>
<div class="balls" id="red"></div>
<div class="balls" id="blue"></div>
```
