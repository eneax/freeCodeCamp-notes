# Use the flex-direction Property to Make a Row

Adding `display: flex` to an element turns it into a flex container. This makes it possible to align any children of that element into rows or columns. You do this by adding the `flex-direction` property to the parent item and setting it to `row` (default value) or `column`.

Creating a row will align the children horizontally, and creating a column will align the children vertically. Other options for `flex-direction` are `row-reverse` and `column-reverse`.

Example:

```html
<style>
  #box-container {
    height: 500px;
    display: flex;
    flex-direction: row-reverse;
  }
  #box-1 {
    background-color: dodgerblue;
    width: 50%;
    height: 50%;
  }

  #box-2 {
    background-color: orangered;
    width: 50%;
    height: 50%;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```
