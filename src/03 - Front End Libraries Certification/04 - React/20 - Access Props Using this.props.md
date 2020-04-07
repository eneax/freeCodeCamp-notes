# Access Props Using this.props

If the child component that we're passing a prop to is an ES6 `class` component, rather than a stateless functional component, we need to use the `this` keyword. 

As we can see from the example below, we passed to the ES6 class component `ReturnTempPassword` a prop called `tempPassword`, so in JSX we can access it by writing `{this.props.tempPassword}`.

```jsx

class ReturnTempPassword extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
        <div>
          <p>Your temporary password is: <strong>{this.props.tempPassword}</strong></p>
        </div>
    );
  }
};

class ResetPassword extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
        <div>
          <h2>Reset Password</h2>
          <h3>We've generated a new temporary password for you.</h3>
          <h3>Please reset this password from your account settings ASAP.</h3>

          <ReturnTempPassword tempPassword='12345678' />
        </div>
    );
  }
};
```
