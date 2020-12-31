# Use tabindex to Specify the Order of Keyboard Focus for Several Elements

The `tabindex` attribute also specifies the exact tab order of elements. This is achieved when the value of the attribute is set to a positive number of `1` or **higher**.

Setting a `tabindex="1"` will bring keyboard focus to that element first. Then it cycles through the sequence of specified `tabindex` values (2, 3, etc.), before moving to default and `tabindex="0"` items.

It's important to note that when the tab order is set this way, it overrides the default order (which uses the HTML source). This may confuse users who are expecting to start navigation from the top of the page. This technique may be necessary in some circumstances, but in terms of accessibility, take care before applying it.

Here's an example:

```html
<body>
  <header>
    <h1>Even Deeper Thoughts with Master Camper Cat</h1>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Blog</a></li>
        <li><a href="">Training</a></li>
      </ul>
    </nav>
  </header>
  <form>
    <label for="search">Search:</label>

    <input type="search" name="search" id="search" tabindex="1" />
    <input
      type="submit"
      name="submit"
      value="Submit"
      id="submit"
      tabindex="2"
    />
  </form>
  <h2>Inspirational Quotes</h2>
  <blockquote>
    <p>
      &ldquo;There's no Theory of Evolution, just a list of creatures I've
      allowed to live.&rdquo;<br />
      - Chuck Norris
    </p>
  </blockquote>
  <blockquote>
    <p>
      &ldquo;Wise men say forgiveness is divine, but never pay full price for
      late pizza.&rdquo;<br />
      - TMNT
    </p>
  </blockquote>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
