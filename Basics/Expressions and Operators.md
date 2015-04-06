
# Expressions and Operators

### Assignment Operators

``` Javascript

x = y
x += y // Can be used to concat strings
x -= y
x *= y
x /= y
x %= y
x <<= y
x >>= y // Signed right shift
x >>>= y // Unsigned right shift
x &= y
x ^= y
x |= y

```

### Destructuring Assignment

``` Javascript

var arr = [1, 2, 3, 4];
var [one, two, three, four] = arr;

```

### Comparison Operators

``` Javascript

x == y
x != y
x === y
x !== y
x > y
x >= y
x < y
x <= y

```

### Arithemtic Operators

``` Javascript
x + y // Can be used to conc strings
x - y
x * y
x / y
x % y
++x
--x
-x
+y

```

### Bitwise Operators

``` Javascript
x & y
x | y
x ^ y
x << y
x >> y
x >>> y
~x

```

- Operands are treated as a set of 32 bits

### Boolean Operators

``` Javascript
x && y // returns x if it can be converted to false, otherwise returns y
x || y // returns x if it can be converted to true, otherwise returns y
!x
```

- `&&` and `||` operators actually return the value of one of their operands, so if these operators are used with non-bools the may return non-bool values. This has tripped me up in the past.
- Logic expressions are evaluated left to right. If we can short circuit the evaluation then the right operands won't be evaluated.

### Ternary Operator

``` Javascript
x ? y : z

```

### Comma Operator

``` Javascript
x, y

```

- Evaluates both operands and returns the last

### Unary Operators

``` Javascript
delete [object | object.prop | object[index] | delete prop] // Four variant only allowed with a `with` statement (but `with` is discouraged), sets to undefined if successful, returns true / false if the deletion is possible or not

typeof operand // Guaranteed to return string
typeof function() {} // "function"
typeof "string" // "string"
typeof 123 // "number"
typeof {} // "object"
typeof [] // "object"
typeof doesntExist // "undefined"
typeof true // "boolean"
typeof null // "object"

void (expression)

if (prop in object) {...}
if (object instanceof Thing) {...}

new Object();

```

- Check out [this table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#Table) for operation precedence.

### Comprehensions

``` Javascript
[for (i of [1, 2, 3, 4]) i*2]; // [2, 4, 8, 8]

```

### Spread

``` Javascript
var things = ['a', 'b', 'c'];
var thingConcat = ['1', ...things, '2']; // ['1', 'a', 'b', 'c', '2']

function func(arg1, arg2, arg3) {...}
func(...things);

```
