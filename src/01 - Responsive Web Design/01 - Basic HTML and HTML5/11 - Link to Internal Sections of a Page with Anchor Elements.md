# Link to Internal Sections of a Page with Anchor Elements

`a` (anchor) elements can also be used to create internal links to jump to different sections within a webpage.

To create an **internal link**, you assign a link's `href` attribute to a **hash** symbol `#` plus the value of the `id` attribute for the element that you want to internally link to (usually further down the page).

You then need to add the same `id` attribute to the element you are linking to. An `id` is an attribute that uniquely describes an element.

Below is an example of an internal anchor link and its target element:

```html
<h2>CatPhotoApp</h2>
<main>
  <a href="#footer">Jump to bottom</a>

  <img
    src="https://bit.ly/fcc-relaxing-cat"
    alt="A cute orange cat lying on its back."
  />

  <p>
    Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching
    attack your ankles chase the red dot, hairball run catnip eat the grass
    sniff. Purr jump eat the grass rip the couch scratched sunbathe, shed
    everywhere rip the couch sleep in the sink fluffy fur catnip scratched.
    Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching
    attack your ankles chase the red dot, hairball run catnip eat the grass
    sniff.
  </p>
  <p>
    Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere
    rip the couch sleep in the sink fluffy fur catnip scratched. Kitty ipsum
    dolor sit amet, shed everywhere shed everywhere stretching attack your
    ankles chase the red dot, hairball run catnip eat the grass sniff. Purr jump
    eat the grass rip the couch scratched sunbathe, shed everywhere rip the
    couch sleep in the sink fluffy fur catnip scratched.
  </p>
  <p>
    Meowwww loved it, hated it, loved it, hated it yet spill litter box, scratch
    at owner, destroy all furniture, especially couch or lay on arms while
    you're using the keyboard. Missing until dinner time toy mouse squeak roll
    over. With tail in the air lounge in doorway. Man running from cops stops to
    pet cats, goes to jail.
  </p>
  <p>
    Intently stare at the same spot poop in the plant pot but kitten is playing
    with dead mouse. Get video posted to internet for chasing red dot leave fur
    on owners clothes meow to be let out and mesmerizing birds leave fur on
    owners clothes or favor packaging over toy so purr for no reason. Meow to be
    let out play time intently sniff hand run outside as soon as door open yet
    destroy couch.
  </p>
</main>

<footer id="footer">Copyright Cat Photo App</footer>
```

When users click the `Jump to bottom` link, they'll be taken to the section of the webpage with the "footer" `id` attribute.
