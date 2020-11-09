# Create a Set of Radio Buttons

`Radio buttons` are a type of input.
We can use radio buttons for questions where the user can give only one answer out of multiple options.

Each of your radio buttons can be nested within its own `label` element.
By wrapping an input element inside of a label element it will automatically associate the radio button input with the label element surrounding it.

All related radio buttons should have the same `name` attribute in order to create a radio button group.
By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.

Example:

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
    <input type="text" placeholder="cat photo URL" required />

    <label for="indoor">
      <input id="indoor" type="radio" name="indoor-outdoor" />Indoor
    </label>

    <label for="outdoot">
      <input id="outdoot" type="radio" name="indoor-outdoor" />Outdoor
    </label>

    <button type="submit">Submit</button>
  </form>
</main>
```
