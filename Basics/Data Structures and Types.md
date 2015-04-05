
# Data Structures and Types

### Data Types

- Primitives:

	- `Boolean`
	- `null`
	- `undefined` (a top-level property)
	- `Number`
	- `String`
	- `Symbol` (ES6)

- `Object`
- `function`

### Data type conversion

- Javascript is dynamic; you don't have to declare the data type for a variable and its type is converted automatically ad lib.
- Numeric values are converted to string values when the `+` operator is used with strings and numbers.
- `parseInt` and `parseFloat` can be used to retrieve a number from a string value. Its best practice to include a radix param (e.g. 10 for decimal, 8 for octal, etc.).
- The unary plus operator can also be used to covert a string value to a number: `console.log(+'1.1' + +'1.1');` will print 2.2.

### Literals

- `Array`: `['value', 'value']`
	- [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) are objects.
	- `['value', , 'value']` contains `undefined` at the index `1`.
	- Best to include `undefined` array elements explicitly.
	- Trailing commas are ignored in array literals, but can cause errors in older browsers so best practice not to use them.
- `Boolean`: `true`, `false`
- `Integers`
	- `123`: decimal
	- `0123`: octal
	- `0x123`: hexidecimal
	- `0b101`: binary
- `Float`
	- `[(+|-)][digits][.digits][(E|e)[(+|-)]digits]`
	- E.g.: `3.14159265`, `1.234`, `-3.1e23`, `.4E23`
- `Object`
	- `{...}`
	- Zero or more key value pairs
	- Object literals should not be used at the beginning of a statement, because the leading brace may be interpreted as the beginning of a block.
	- If an object key is not a valid identifier it must be enclosed in quotes and can only be accessed using the `[]` notation, not the dot notation.
- `String`: `"string"`, `'string'`
	- You can call any methods of the `String` object on string literals. Js will temporarily convert the literal to a string object, calls the method and then dscards the object.
	- Best practice to use string literals over the `String` object directly unless required.
	- Chars can be escaped: `'c:\\temp'`, etc
	- Line breaks can be escaped similarly:

	``` Javascript

	var str = "broken \
	across \
	lines";

	```
