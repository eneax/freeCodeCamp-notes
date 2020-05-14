# Escaping Literal Quotes in Strings

In order to define a `string`, we must do it by starting and ending with either single or double quotes.
Problems, however, might arise, if we have to include a literal quote; " or ' inside the `string`:

<!-- prettier-ignore -->
```js
var myStringVariable = "I am a "double quoted" string inside "double quotes"."; 
```

The code above will generate an error on the console: `Uncaught SyntaxError: Unexpected identifier`, since JavaScript doesn't know where the string variable ends.

To fix this problem, we can escape the quote from being considered as the end of the string quote by using the backslash `\` in front of the quote:

<!-- prettier-ignore -->
```js
var myStringVariable = "I am a \"double quoted\" string inside \"double quotes\"."; 
```
