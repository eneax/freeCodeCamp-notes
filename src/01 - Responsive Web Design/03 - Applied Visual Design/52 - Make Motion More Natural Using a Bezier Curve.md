# Make Motion More Natural Using a Bezier Curve

This challenge animates an element to replicate the movement of a ball being **juggled**.
The `animation-timing-function` automatically loops at every keyframe when the `animation-iteration-count` is set to infinite. Since there is a keyframe rule set in the middle of the animation `duration` (at `50%`), it results in two identical animation progressions at the upward and downward movement of the ball.

The following cubic Bezier curve simulates a juggling movement: `cubic-bezier(0.3, 0.4, 0.5, 1.6);`.

Example:

```html
<style>
  .balls {
    border-radius: 50%;
    position: fixed;
    width: 50px;
    height: 50px;
    top: 60%;
    animation-name: jump;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #red {
    background: red;
    left: 25%;
    animation-timing-function: linear;
  }
  #blue {
    background: blue;
    left: 50%;
    animation-timing-function: ease-out;
  }
  #green {
    background: green;
    left: 75%;
    animation-timing-function: cubic-bezier(0.311, 0.441, 0.444, 1.649);
  }

  @keyframes jump {
    50% {
      top: 10%;
    }
  }
</style>
<div class="balls" id="red"></div>
<div class="balls" id="blue"></div>
<div class="balls" id="green"></div>
```

**Notice** that the value of y2 is larger than 1. Although the cubic Bezier curve is mapped on a 1 by 1 coordinate system, and it can only accept x values from 0 to 1, the y value can be set to numbers larger than one. This results in a bouncing movement that is ideal for simulating the juggling ball.
