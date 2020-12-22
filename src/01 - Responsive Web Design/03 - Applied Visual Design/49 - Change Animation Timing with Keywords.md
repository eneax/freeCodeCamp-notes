# Change Animation Timing with Keywords

In CSS animations, the `animation-timing-function` property controls how quickly an animated element changes over the duration of the animation. If the animation is a car moving from point A to point B in a given time (your `animation-duration`), the `animation-timing-function` says how the car accelerates and decelerates over the course of the drive.

There are a number of predefined keywords available for popular options:

- `ease` (the default value), starts slow, speeds up in the middle, and then slows down again in the end
- `ease-out` is quick in the beginning then slows down
- `ease-in` is slow in the beginning, then speeds up at the end
- `linear` applies a constant animation speed throughout.

Example:

```html
<style>
  .balls {
    border-radius: 50%;
    background: linear-gradient(35deg, #ccffff, #ffcccc);
    position: fixed;
    width: 50px;
    height: 50px;
    margin-top: 50px;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #ball1 {
    left: 27%;
    animation-timing-function: linear;
  }
  #ball2 {
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

<div class="balls" id="ball1"></div>
<div class="balls" id="ball2"></div>
```
