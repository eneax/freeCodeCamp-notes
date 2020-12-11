# Lock an Element to its Parent with Absolute Positioning

Another option for the CSS position property is `absolute`, which locks the element in place **relative to its parent container**. Unlike the relative position, this **removes** the element from the normal flow of the document, so surrounding items ignore it.

The CSS offset properties (`top` or `bottom` and `left` or `right`) are used to adjust the position.

**Note**: with absolute positioning, the element will be locked relative to its closest positioned ancestor. If you forget to add a `position` rule to the parent item, (this is typically done using `position: relative;`), the browser will _keep looking up the chain_ and ultimately default to the `body` tag.

Example:

```html
<style>
  #searchbar {
    position: absolute;
    top: 50px;
    right: 50px;
  }
  section {
    position: relative;
  }
</style>

<body>
  <h1>Welcome!</h1>
  <section>
    <form id="searchbar">
      <label for="search">Search:</label>
      <input type="search" id="search" name="search" />
      <input type="submit" name="submit" value="Go!" />
    </form>
  </section>
</body>
```
