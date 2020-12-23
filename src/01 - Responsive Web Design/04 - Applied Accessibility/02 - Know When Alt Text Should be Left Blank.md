# Know When Alt Text Should be Left Blank

Sometimes images are grouped with a caption already describing them, or are used for decoration only. In these cases `alt` text may seem redundant or unnecessary.

In situations when an image is already explained with text content, or does not add meaning to a page, the img still needs an `alt` attribute, but it can be set to an empty string. Here's an example: `<img src="visualDecoration.jpeg" alt="">`

**Background images** usually fall under the 'decorative' label as well. However, they are typically applied with CSS rules, and therefore not part of the markup screen readers process.

**Note**: For images with a caption, you may still want to include `alt` text, since it helps search engines catalog the content of the image.

Example:

```html
<h1>Deep Thoughts with Master Camper Cat</h1>
<article>
  <h2>Defeating your Foe: the Red Dot is Ours!</h2>
  <p>To Come...</p>
</article>

<img src="samuraiSwords.jpeg" alt="" />

<article>
  <h2>Is Chuck Norris a Cat Person?</h2>
  <p>To Come...</p>
</article>
```
