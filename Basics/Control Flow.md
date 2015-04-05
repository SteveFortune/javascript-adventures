
# Control Flow

### Block

``` Javascript

{
	// This is a block
}

```

- Block scoping is only introduced in ES6 with `let`

### If.. else

``` Javascript

if (...) {
	...
} else if (...) {
	...
} else if (...) {
	...
} else {
	...
}

```

- Best practice, if you're using simple assignment in an if condition to enclose it in 2 additional parentheses : if ((x = 123)) {...}
- The following are falsy values:

	- NaN
	- undefined
	- null
	- 0
	- "" or ''
	- false

### Switch

``` Javascript

switch (...) {
	case ...:
		...
		[break;]
	case ...:
		...
		[break;]
	default:
		...
		[break;]
}

```

### Exceptions

``` Javascript

function throwException() {
	throw "An error";
}

try {
	throwException();
} catch (e) {
	console.log(e); // Prints "An error"
} finally {
	console.log("Done..");
	return false; // return and throw statements in the finally block supersede statements in the try and catch blocks
}

```

- Anything can be thrown in javascript.
- Typical to throw ECMAScript error objects.
- Exceptions bubble up to parent `try..catch` blocks in nested environments.

### Loops

``` Javascript

for (var i = 0; i < 10; ++i) {
	console.log(i);
}

var i = 100;
do {
	// Will be executed at least once
	--i;
} while (i > 0);

while ((ln = readFile()) !== EOL) {
	...
}

label: while (true) ;

break;
break label;
continue;
continue label;

for (let prop in obj) {
	if (obj.hasOwnProperty(prop)) {
		...
	}
}

let arr = [1, 2, 3, 4, 5];
for (let value in arr) {
	...
}

```
