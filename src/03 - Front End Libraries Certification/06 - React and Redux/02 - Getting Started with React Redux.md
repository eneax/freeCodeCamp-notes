# Getting Started with React Redux

`React` is a library for building user interfaces. We provide the data and React renders the view in a predictable way.
`Redux` is a predictable state container for JavaScript apps that we use to simplify the management of our application's state.

React components can manage their state locally as `stateful components`. However, when dealing with larger applications,
it's better to keep all the app state in a single location with Redux.
Thus, we can combine both React and Redux, using the `react-redux` package, in order to have a single Redux `store` that manages the state of our entire app. The React components will subscribe only to the pieces of state in the store that are relevant to them.
Additionally, we can dispatch actions directly from our React components, that will at the end trigger store updates.

Before integrating React with Redux, we can start by creating a simple React stateful component with an initial state equal to : `{input: "", messages: []}`:

```js
class DisplayMessages extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      input: "",
      messages: []
    };
  }

  render() {
    return <div />;
  }
}
```
