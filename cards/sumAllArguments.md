Create a function that accepts any number of integer arguments, and returns the sum of all the arguments.

## Setup

```js
function sum() {
  return;
}

console.log(sum(1)); // 1
console.log(sum(1, 2)); // 3
console.log(sum(1, 2, 3)); // 6
console.log(sum(1, 2, 3, 4)); // 10
```

---

## using the spread operator

```js
function sum() {
  return [...arguments].reduce((total, n) => {
    return total + n;
  }, 0);
}
```

## using call()

```js
function sum() {
  return [].slice.call(arguments).reduce((total, n) => {
    return total + n;
  }, 0);
}
```
