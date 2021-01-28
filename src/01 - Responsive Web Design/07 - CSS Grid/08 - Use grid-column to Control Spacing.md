# Use grid-column to Control Spacing

Up to this point, all the properties that have been discussed are for grid containers. The `grid-column` property is the first one for use on the grid items themselves.

The hypothetical horizontal and vertical lines that create the grid are referred to as `lines`. These `lines` are numbered starting with `1` at the top left corner of the grid and move right for columns and down for rows, counting upward.

To control the amount of columns an item will consume, you can use the `grid-column` property in conjunction with the line numbers you want the item to start and stop at.

Here's an example: `grid-column: 1 / 3;`
This will make the item start at the first vertical line of the grid on the left and span to the 3rd line of the grid, consuming two columns.

Example:

```html
<style>
  .item1 {
    background: LightSkyBlue;
  }
  .item2 {
    background: LightSalmon;
  }
  .item3 {
    background: PaleTurquoise;
  }
  .item4 {
    background: LightPink;
  }

  .item5 {
    background: PaleGreen;
    grid-column: 2 / 4; /* It consumes the last two columns of the grid */
  }

  .container {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
  }
</style>

<div class="container">
  <div class="item1">1</div>
  <div class="item2">2</div>
  <div class="item3">3</div>
  <div class="item4">4</div>
  <div class="item5">5</div>
</div>
```
