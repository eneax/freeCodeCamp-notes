# Render React on the Server with renderToString

Up to this point, we have seen how to render a React component on the client. However, since React is just JavaScript and we can run JavaScript on the server with Node.js, we can render React on the Server with `renderToString()`.

Rendering on the server can be done for two main reasons:

1. Search Engine Indexing

Since we can render the initial HTML markup on the server and then send it to the client, the initial page load will contain all of the page's markup so it can be crawled by search engines.

2. Faster initial page load experience

This is achieved due to the fact that the rendered HTML will be smaller than the JavaScript code of the entire app.

Here is an example of the `renderToString()` in action:

```jsx
class App extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <div />;
  }
}

ReactDOMServer.renderToString(<App />);
```
