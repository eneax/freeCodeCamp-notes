# Link to External Pages with Anchor Elements

You can use `a` (anchor) **elements** to link to content outside of your web page.
`a` elements need a destination web address called an `href` **attribute** and an anchor text.

Example:

```html
<h2>CatPhotoApp</h2>
<main>
  <a href="https://freecatphotoapp.com">cat photos</a>

  <img
    src="https://bit.ly/fcc-relaxing-cat"
    alt="A cute orange cat lying on its back."
  />

  <p>
    Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching
    attack your ankles chase the red dot, hairball run catnip eat the grass
    sniff.
  </p>
  <p>
    Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere
    rip the couch sleep in the sink fluffy fur catnip scratched.
  </p>
</main>
```

The browser will display the text "cat photos" as a link you can click.
And that link will take you to the web address `https://www.freecodecamp.org`.

**Note**: if you want the linked document to open in a new window tab, add the `target="_blank"` attribute to the anchor tag. This practice, however, causes performance and security issues for your website. Adding `rel="noopener"` or `rel="noreferrer"` to your `target="_blank"` links avoids these issues.
