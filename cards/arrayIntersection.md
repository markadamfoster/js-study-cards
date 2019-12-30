# Intersection of an Array

You are given two arrays of integers as arguments. Return an array of integers which represents the intersection - the common elements from the original two arrays.

## Setup
```js
const solve = (arrOne, arrTwo) => {
  return;
};

console.log(solve([1, 2, 3, 4, 5], [4, 2])); // [2,4]
console.log(solve([2, 5, 6, 9, 13, 1], [1, 6, 13, 7])); // [6,13,1]
console.log(solve([1, -2, 3, -4, 5], [-4, -2])); // [-2,-4]
```

---
```js
const solve = (arrOne, arrTwo) => {
  return arrOne.filter(n => arrTwo.includes(n));
};
```