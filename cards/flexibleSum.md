Write a sum method which will work properly when invoked using either syntax below.

```js
console.log(sum(2,3));   // Outputs 5
console.log(sum(2)(3));  // Outputs 5
```

---

(I don't 100% understand this syntax yet)

```js
function sum(a) {
  if (arguments.length === 2) {
    return arguments[0] + arguments[1]
  }
  return function(b) {
    return a + b
  }
}

function sum2(a, b) {
  if (b !== undefined) {
    return a + b
  }

  return function(b) {
    return a + b
  }
}

console.log(sum(2,3));   // Outputs 5
console.log(sum(2)(3));  // Outputs 5

console.log(sum2(2,3));   // Outputs 5
console.log(sum2(2)(3));  // Outputs 5
```