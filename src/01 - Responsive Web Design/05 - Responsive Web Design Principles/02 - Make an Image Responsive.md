# Make an Image Responsive

Making images responsive with CSS is actually very simple. You just need to add these properties to an image:

```css
img {
  max-width: 100%;
  height: auto;
}
```

The `max-width` of `100%` will make sure the image is never wider than the container it is in, and the `height` of `auto` will make the image keep its original aspect ratio.

Example:

```html
<style>
  .responsive-img {
    max-width: 100%;
    height: auto;
  }

  img {
    width: 600px;
  }
</style>

<img
  class="responsive-img"
  src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg"
  alt="freeCodeCamp stickers set"
/>
<img
  src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg"
  alt="freeCodeCamp stickers set"
/>
```
