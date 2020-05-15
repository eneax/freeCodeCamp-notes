# Quoting Strings with Single Quotes

JavaScript supports both single and double quotes, as long as we start and end the string variable with the same type of quotes. Moreover, we can fix the issue of using a literal quote inside a string variable, thanks to the backslash `\` character.

However, it's important to not abuse backslash `\` character; since it can make our code more difficult to read.
For this reason, we can always use single quotes for our string variables and use double quote only when needed inside the variable, like in the code below:

```js
var myStringVariable =
  '<a href="http://www.example.com" target="_blank">Example Link</a>';
```
