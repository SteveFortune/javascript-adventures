
# Array Notes

- `Array.length` must be an integer, otherwise a RangeError is thrown.
- Array access notation `[]` can be used to access properties as well as elements at given indexes.
- This is because the array impl actually stores the elements as value-pairs to the index key.
- Length always returns the index of the last elements + 1, e.g `var arr = []; arr[30] = 1; arr.length;` `arr.length` is `31`.
- Length property is mutable.
- Setting it to a value that is shorter than the current length of the array truncates the trailing array elements.
- When iterating over an array using `forEach` method, `undefined` elements will not be omitted if they have been set manually (e.g. `var arr = [1, undefined, 2];`) otherwise will be omitted.
- Not advised to iterate over arrays using `for...in` because they are actually objects and all of their enumerable properties will be listed.
- Iterative array methods have an options `thisObject` parameter, which, if passed, will become the value of `this` in the callback. Note that I can imagine arrow functions make this obsolete.
- Checkout [iterators and generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators)!
