# Center an Element Horizontally Using the margin Property

Another positioning technique is to center a block element horizontally. One way to do this is to set its `margin` to a value of `auto`.

```html
<style>
  div {
    background-color: blue;
    height: 100px;
    width: 100px;
    margin: auto;
  }
</style>
<div></div>
```

**Note**: This method works for images, too. Images are inline elements by default, but can be changed to block elements when you set the display property to block.
