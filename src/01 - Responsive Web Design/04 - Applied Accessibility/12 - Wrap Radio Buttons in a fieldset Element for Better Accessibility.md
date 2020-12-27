# Wrap Radio Buttons in a fieldset Element for Better Accessibility

Each choice is given a label with a `for` attribute tying to the `id` of the corresponding item as covered in the last challenge. Since **radio buttons** often come in a group where the user must choose one, there's a way to semantically show the choices are part of a set.

The `fieldset` tag surrounds the entire grouping of radio buttons to achieve this. It often uses a legend tag to provide a description for the grouping, which is read by screen readers for each choice in the `fieldset` element.

The `fieldset` wrapper and `legend` tag are not necessary when the choices are self-explanatory, like a gender selection. Using a label with the `for` attribute for each radio button is sufficient.

Here's an example:

```html
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <section>
    <form>
      <p>Sign up to receive Camper Cat's blog posts by email here!</p>
      <label for="email">Email:</label>
      <input type="text" id="email" name="email" />

      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie" />
        <label for="newbie">Newbie Kitten</label><br />
        <input
          id="intermediate"
          type="radio"
          name="levels"
          value="intermediate"
        />
        <label for="intermediate">Developing Student</label><br />
        <input id="master" type="radio" name="levels" value="master" />
        <label for="master">Master</label>
      </fieldset>

      <input type="submit" name="submit" value="Submit" />
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>
      The internet is littered with varying opinions on nutritional paradigms,
      from catnip paleo to hairball cleanses. But let's turn our attention to an
      often overlooked fitness fuel, and examine the protein-carb-NOM trifecta
      that is lasagna...
    </p>
  </article>
  <img src="samuraiSwords.jpeg" alt="" />
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>
      Felines the world over have been waging war on the most persistent of
      foes. This red nemesis combines both cunning stealth and lightning speed.
      But chin up, fellow fighters, our time for victory may soon be near...
    </p>
  </article>
  <img src="samuraiSwords.jpeg" alt="" />
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>
      Chuck Norris is widely regarded as the premier martial artist on the
      planet, and it's a complete coincidence anyone who disagrees with this
      fact mysteriously disappears soon after. But the real question is, is he a
      cat person?...
    </p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
