# Merge and sort two arrays of integers

You are given two arrays of integers as arguments. Merge the two arrays into a single array sorted in ascending numerical order, with all duplicates removed.

### Setup

```js
const solve = (arrOne, arrTwo) => {
  return;
};

console.log(solve([1, 2, 3, 4], [8, 9, 2, 4])); // [1,2,3,4,8,9]
console.log(solve([-1, 2, 3, 4], [1, 8, 9, 2, 4])); // [-1,1,2,3,4,8,9]
```

---

```js
const solve = (arrOne, arrTwo) => {
  return [...new Set([...arrOne, ...arrTwo])].sort((a, b) => (a < b ? -1 : 1));
};
```
