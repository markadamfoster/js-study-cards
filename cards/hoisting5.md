What does the following code output? (and what is the technical explanation of why we get that output?)

```js
console.log(x);
var x = 5;
console.log(x);
console.log(y);
```

---

`undefined`
`5`
`ReferenceError: y is not defined`

This is because the variable declaration is hoisted, but not the assignment. The code the JavaScript engine actually runs looks more like this:

```js
var x;
console.log(x); // -> undefined
x = 5;
console.log(x); // -> 5
console.log(y); // -> Uncaught ReferenceError: y is not defined
```