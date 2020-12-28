# Make Elements Only Visible to a Screen Reader by Using Custom CSS

Have you noticed that all of the applied accessibility challenges so far haven't used any CSS? This is to show the importance of a logical document outline, and using semantically meaningful tags around your content before introducing the visual design aspect.

However, CSS's magic can also improve accessibility on your page when you want to visually hide content meant only for screen readers. This happens when information is in a visual format (like a chart), but screen reader users need an alternative presentation (like a table) to access the data. CSS is used to position the screen reader-only elements off the visual area of the browser window.

Here's an example of the CSS rules that accomplish this:

```html
<head>
  <style>
    .sr-only {
      position: absolute;
      left: -10000px;
      width: 1px;
      height: 1px;
      top: auto;
      overflow: hidden;
    }
  </style>
</head>
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <section>
    <h2>Master Camper Cat's Beginner Three Week Training Program</h2>
    <figure>
      <!-- Stacked bar chart of weekly training -->
      <p>[Stacked bar chart]</p>
      <br />
      <figcaption>
        Breakdown per week of time to spend training in stealth, combat, and
        weapons.
      </figcaption>
    </figure>
    <table class="sr-only">
      <caption>
        Hours of Weekly Training in Stealth, Combat, and Weapons
      </caption>
      <thead>
        <tr>
          <th></th>
          <th scope="col">Stealth &amp; Agility</th>
          <th scope="col">Combat</th>
          <th scope="col">Weapons</th>
          <th scope="col">Total</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Week One</th>
          <td>3</td>
          <td>5</td>
          <td>2</td>
          <td>10</td>
        </tr>
        <tr>
          <th scope="row">Week Two</th>
          <td>4</td>
          <td>5</td>
          <td>3</td>
          <td>12</td>
        </tr>
        <tr>
          <th scope="row">Week Three</th>
          <td>4</td>
          <td>6</td>
          <td>3</td>
          <td>13</td>
        </tr>
      </tbody>
    </table>
  </section>
  <section id="stealth">
    <h2>Stealth &amp; Agility Training</h2>
    <article>
      <h3>Climb foliage quickly using a minimum spanning tree approach</h3>
    </article>
    <article><h3>No training is NP-complete without parkour</h3></article>
  </section>
  <section id="combat">
    <h2>Combat Training</h2>
    <article>
      <h3>Dispatch multiple enemies with multithreaded tactics</h3>
    </article>
    <article>
      <h3>Goodbye, world: 5 proven ways to knock out an opponent</h3>
    </article>
  </section>
  <section id="weapons">
    <h2>Weapons Training</h2>
    <article>
      <h3>Swords: the best tool to literally divide and conquer</h3>
    </article>
    <article>
      <h3>Breadth-first or depth-first in multi-weapon training?</h3>
    </article>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

**Note**
The following CSS approaches will NOT do the same thing:

- `display: none;` or `visibility: hidden;` hides content for everyone, including screen reader users
- Zero values for pixel sizes, such as `width: 0px;` and `height: 0px;` removes that element from the flow of your document, meaning screen readers will ignore it.
