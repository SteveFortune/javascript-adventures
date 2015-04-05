
# Functions

``` Javascript

function func1(arg1, arg2) {
	return 123;
}

var func2 = function(arg) {
	return 123;
}

var func3 = function f3(arg) {
	if (arg === true) {
		f3(false);
	}
}

```

- Objects (including arrays) are passed by reference, primitives are passed my value
- Functions in javascript are first class values.
- Function declarations are hoisted like variables iff they are declared with the `function name() {...}` syntax.
- Variables defined within the scope of a function cannot be accessed outside of the enclosing scope.
- Functions can access all of the variables that are available in their parent scope (scope chain).
- `arguments.callee` can be used to access the currently executing function. This should be avoided and in ES5 strict mode it is forbidden.
- See [here](http://stackoverflow.com/questions/111102/how-do-javascript-closures-work) for specifics of closures. See [here](https://hacks.mozilla.org/2012/11/tracking-down-memory-leaks-in-node-js-a-node-js-holiday-season/) for how closures can cause memory leaks.
- If 2 variables within the scope chain have the same name, we have a naming conflict. In this scenario, the variable of the inner-most scope is used.
- Arguments are accessible in a function via the `arguments` array-like object, e.g. `arguments[0]` accesses the first argument. This way you can detect whether variadic arguments are passed.

### ES6 Function Features

- Default parameters

	``` Javascript
	function mult(a, b = 1) {
		return a*b;
	}
	```

- Rest parameters

	``` Javascript
	function mult(a, ...bs) {
		return bs.map(function(b) {
			return a*b;
		});
	}
	```

- Arrow functions

	``` Javascript
	function mult(a, ...bs) {
		return bs.map(b => a*b);
	}
	```
