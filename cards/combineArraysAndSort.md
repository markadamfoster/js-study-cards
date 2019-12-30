You are given two sorted arrays of integers as arguments. Return a new array combining elements from both arrays in sorted order.

There will never be duplicate integers in either array.

## Setup

```js
const solve = (arrOne, arrTwo) => {
  return;
};

console.log(solve([1, 10, 20], [2, 3, 15])); // [1,2,3,10,15,20]
console.log(solve([-1, 0, 5], [-2, 3, 15])); // [-2,-1,0,3,5,15]
```

---

```js
const solve = (arrOne, arrTwo) => {
  return [...arrOne, ...arrTwo].sort((a, b) => (a-b));
};
```