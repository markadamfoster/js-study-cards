# Create a Multiplication Table

You are given an integer N as an argument. Return a two dimensional array containing arrays of integers that make up a multiplication table from 1x1 to NxN.

## Setup
```js
const solve = n => {
  return;
};

console.log(solve(4));
/*
  [[1, 2, 3, 4],
  [2, 4, 6, 8],
  [3, 6, 9, 12],
  [4, 8, 12, 16]]
*/
```

---
```js
const solve = n => {
  const result = [];

  for (let i = 1; i <= n; i++) {
    let subArr = [];

    for (let k = 1; k <= n; k++) {
      subArr.push(i * k);
    }

    result.push(subArr);
  }

  return result;
};
```