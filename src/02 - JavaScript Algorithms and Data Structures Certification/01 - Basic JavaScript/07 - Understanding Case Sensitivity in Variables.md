# Understanding Case Sensitivity in Variables

In JavaScript capitalization matter! In fact, all variables and function names are case sensitive.
For instance, if we take into consideration the following three variable names: `MYVAR`, `MyVar` and `myvar`, they all represent three different variables.

Even if the three name above are all valid names for a variable in JavaScript, it's best practice to write variable names in `camelCase`. Thus, if we have to deal with a multi-word variable name, we write the first word in `lowercase` and the first letter of each subsequent word as `capitalized`.

Examples:

```js
var myPhone;
var myPhoneNumber;
var myPersonalPhoneNumber;
```
