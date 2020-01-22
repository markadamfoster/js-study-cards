You are given a non-negative integer as an argument. Add each digit of the integer together and return the sum.

## Setup
```js
const solve = intArg => {
  return;
};

console.log(solve(6368206)); // 31
```

---

```js
const solve = intArg => {
  return intArg
    .toString()
    .split("")
    .reduce((sum, n) => {
      return parseInt(n) + sum;
    }, 0);
};
```