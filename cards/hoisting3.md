What will this code output to the console and why?

```js
(function(){
	var a = b = 3
})()


console.log("a defined? " + (typeof a !== 'undefined'))
console.log("b defined? " + (typeof b !== 'undefined'))
```

---

The line `var a = b = 3` is actually shorthand for:

```js
b = 3;
var a = b;
```

Since strict mode is not enabled, and `b` does not exist in the function's scope, it would be auto-created in the global scope. Thus, the console output would be:

```js
a defined? false
b defined? true
```

If strict mode had been enabled, it would generate a runtime error of `ReferenceError: b is not defined`.
