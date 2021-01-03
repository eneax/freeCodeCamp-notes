# Use a Retina Image for Higher Resolution Displays

With the increase of internet connected devices, their sizes and specifications vary, and the displays they use could be different externally and internally. **Pixel density** is an aspect that could be different on one device from others and this density is known as Pixel Per Inch (**PPI**) or Dots Per Inch (**DPI**).

The most famous such display is the one known as a "_Retina Display_" on the latest Apple MacBook Pro notebooks, and recently iMac computers. Due to the difference in pixel density between a "Retina" and "Non-Retina" displays, some images that have not been made with a High-Resolution Display in mind could look "pixelated" when rendered on a High-Resolution display.

The simplest way to make your images properly appear on High-Resolution Displays, such as the MacBook Pros "retina display" is to define their `width` and `height` values as only half of what the original file is.

Here is an example of an image that is only using half of the original height and width:

```html
<style>
  img {
    /* both the original height and the original width are 200px */
    height: 100px;
    width: 100px;
  }
</style>

<img
  src="https://s3.amazonaws.com/freecodecamp/FCCStickers-CamperBot200x200.jpg"
  alt="freeCodeCamp sticker that says 'Because CamperBot Cares'"
/>
```
