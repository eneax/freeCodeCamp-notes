# Escape Sequences in Strings

Other than quotes, in JavaScript, we can escape many other characters inside a string.
The main reason to do this is to use multiple quotes in a string without JavaScript misinterpreting our code.

| Code | Output          |
| ---- | --------------- |
| \'   | single quote    |
| \"   | double quote    |
| \\   | backslash       |
| \n   | newline         |
| \r   | carriage return |
| \t   | tab             |
| \b   | word boundary   |
| \f   | form feed       |

```js
var myStringVariable = "FirstLine\n\t\\SecondLine\nThirdLine";

/*
"FirstLine
	\SecondLine
ThirdLine"
*/
```
