# Create a Set of Checkboxes

`Checkboxes` are a type of input that are commonly used in forms with questions that may have more than one answer.

Each of your checkboxes can be nested within its own `label` element.
By wrapping an `input` element inside of a `label` element, it will automatically associate the `checkbox` input with the `label` element surrounding it.

**Note**: It is considered best practice to explicitly define the relationship between a checkbox input and its corresponding label by setting the `for` attribute on the label element to match the `id` attribute of the associated input element.

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
    <label for="indoor"
      ><input id="indoor" type="radio" name="indoor-outdoor" /> Indoor</label
    >
    <label for="outdoor"
      ><input id="outdoor" type="radio" name="indoor-outdoor" /> Outdoor</label
    ><br />

    <label for="loving">
      <input type="checkbox" id="loving" name="personality" /> Loving
    </label>
    <label for="adorable">
      <input type="checkbox" id="adorable" name="personality" /> Adorable
    </label>
    <label for="cute">
      <input type="checkbox" id="cute" name="personality" /> Cute
    </label>

    <input type="text" placeholder="cat photo URL" required />
    <button type="submit">Submit</button>
  </form>
</main>
```
