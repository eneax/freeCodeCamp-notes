# Add a Submit Button to a Form

Let's add a submit `button` to the form. Clicking this button will send the data from the form to the URL you specified with your form's action attribute.

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#">
    <img
      src="https://bit.ly/fcc-relaxing-cat"
      alt="A cute orange cat lying on its back."
    />
  </a>

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

  <form action="https://freecatphotoapp.com/submit-cat-photo">
    <input type="text" placeholder="cat photo URL" />
    <button type="submit">Submit</button>
  </form>
</main>
```