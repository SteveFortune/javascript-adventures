
# Variables

### Declaration

- Names of variables are [identifiers](https://developer.mozilla.org/en-US/docs/Glossary/Identifier)
- Identifiers must start with a letter, underscore or collar sign.
- Case sensitive (as is javascript as a language)
- ISO 8859-1, Unicode letters, and Unicode escape sequences can be used as characters in identifiers.

``` Javascript

let validVar;
let _validVar;
let $_validVar;
let ValidVar;
let vãlidVér;
let π; // @note Remember to enable utf-8 in the HTML doc: `<meta charset="utf-8">` or `<script ... charset="utf-8">`

```

1. Variables can be declared with `var`. These variables can be declared locally or globally. Variables declared with `var` that are not declared at the global scope are local to the scope of function that they're declared in.
2. Local variables can be declared with `let`. These variables are within the scope of their block.
3. Global variables can be declared without `var` or `let`. These variables cannot be changed at the local level. Generates a strict warning and shouldn't be used.

``` Javascript

// 1

var globalVar = 123;

function func() {
	if (...) {
		var localVar = 44;
	}
	console.log(localVar); // Will print 44
}

// 2

if (...) {
	let blockScoped = 123;
}

console.log(blockScoped); // Will print undefined

// 3

badThing = 23; // Generates strict error

```

### Evaluation

1. Variables declared with `var` or `let` with no initial value will be `undefined`.
2. Access to an undeclared variables will throw a `ReferenceError`.
3. Numerous ways of checking whether a variable is valid for use. From [this source](http://stackoverflow.com/questions/3390396/how-to-check-for-undefined-in-javascript).
4. `undefined` is a falsey value, and evaluates to `NaN` when used in a numeric context.
5. `null` is a falsey value and evaluates to `0` when used in a numeric context.

``` Javascript

// 1.

var variable1;
let variable2;

console.log(variable1); // undefined
console.log(variable2); // undefined

// 2.

console.log(notDeclared); // Throws ReferenceError

// 3.

if ("someProp" in someObj) {...}
if (typeof someVar !== 'undefined') {...}
if (someVar !== undefined) {...} // Note < ECMAScript 5 undefined is mutable so can be overwritten. Safest to check with `typeof`

// 4.

var variable3;

if (!variable3) {...} // Will execute if block
console.log(variable3 + 10) // Will print NaN

// 5.

var variable4 = null;

if (!variable4) {...} // Will execute if block
console.log(variable4 + 1) // Will print 1

```

### Variable Hoisting

- Variable declarations are 'hoisted' to the top of their enclosing statement.
- Variable initialization are not.
- You can refer to a variable declared late without a `ReferencedError`.
- Place `var` statements as near to the top of the function as possible for clarity.

``` Javascript

if (typeof variable === 'undefined') {...} // True, no error

var variable;

```
