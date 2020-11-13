# Use CSS Selectors to Style Elements

There are hundreds of CSS properties that we can use to change the way an element looks on the page. When we used `<h2 style="color: red;">CatPhotoApp</h2>`, we were styling that **individual** `h2` element with inline CSS.

That's one way to specify the style of an element, but there's a better way to apply CSS.
At the top of your code, create a `style` block and inside of it, you can create a CSS selector for **all** `h2` elements.

```html
<style>
  h2 {
    color: red;
  }
</style>
```

**Note**: it's important to have both opening and closing curly braces (`{` and `}`) around each element's style rule(s). You also need to make sure that your element's style definition is between the opening and closing `style` tags. Finally, be sure to add a `semicolon` to the end of each of your element's style rules.

Example:

```html
<style>
  h2 {
    color: blue;
  }
</style>

<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"
    ><img
      src="https://bit.ly/fcc-relaxing-cat"
      alt="A cute orange cat lying on its back."
  /></a>

  <div>
    <p>Things cats love:</p>
    <ul>
      <li>cat nip</li>
      <li>laser pointers</li>
      <li>lasagna</li>
    </ul>
    <p>Top 3 things cats hate:</p>
    <ol>
      <li>flea treatment</li>
      <li>thunder</li>
      <li>other cats</li>
    </ol>
  </div>

  <form action="https://freecatphotoapp.com/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked /> Indoor</label>
    <label><input type="radio" name="indoor-outdoor" /> Outdoor</label><br />
    <label><input type="checkbox" name="personality" checked /> Loving</label>
    <label><input type="checkbox" name="personality" /> Lazy</label>
    <label><input type="checkbox" name="personality" /> Energetic</label><br />
    <input type="text" placeholder="cat photo URL" required />
    <button type="submit">Submit</button>
  </form>
</main>
```
