What does the following code output, and why?

```js
console.log(square(5));

function square(n) { return n * n; }
```

Related, what does the following code output, and why?

```js
console.log(square(5));
 
var square = function(n) { 
  return n * n; 
}
```

---
## Question 1:
```js
25
```

This is because in JavaScript function declarations are hoisted. So the interpreter (essentially) sees it as:

```js
function square(n) { return n * n; }

console.log(square(5));
```

## Question 2:
`TypeError: square is not a function`

The variable declaration is hoisted, but not the assignment. So `square` exists, but it's `undefined`.