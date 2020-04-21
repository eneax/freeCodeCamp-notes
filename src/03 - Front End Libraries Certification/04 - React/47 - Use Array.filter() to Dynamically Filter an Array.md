# Use Array.filter() to Dynamically Filter an Array

Another array method very common in React is `filter()`, which filters the contents of an array based on a specified condition and returns a new array.

For instance, if we have an array of users, containing the boolean property `online`, we can filter only those users that are currently online:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      users: [
        {
          username: "Jeff",
          online: true
        },
        {
          username: "Alan",
          online: false
        },
        {
          username: "Mary",
          online: true
        },
        {
          username: "Jim",
          online: false
        },
        {
          username: "Sara",
          online: true
        },
        {
          username: "Laura",
          online: true
        }
      ]
    };
  }
  render() {
    const users = this.state.users;
    const usersOnline = users.filter(user => user.online);
    const renderOnline = usersOnline.map(user => (
      <li key={user.username}>{user.username}</li>
    ));

    return (
      <div>
        <h1>Current Online Users:</h1>
        <ul>{renderOnline}</ul>
      </div>
    );
  }
}
```
