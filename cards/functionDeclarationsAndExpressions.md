Write an example and talk about the differences between a function expression and a function declaration.

---


```js
// function declaration
function myFunc() {
  // code
}

// function expression
var myFunc2 = function() {
  // code
}
```

The biggest difference is with hoisting. For a function declaration, the entire declaration gets hoisted, as opposed to a function expression, where just the variable declaration gets hoisted.