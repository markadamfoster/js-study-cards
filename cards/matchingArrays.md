You are given two arrays of integers as arguments. Return true if they contain the exact same elements in any order.

## Setup

```js
const solve = (arrOne, arrTwo) => {
  return;
};

console.log(solve([1, 2, 7], [7, 1, 2])); // true
console.log(solve([5, 7], [7, 1])); // false
console.log(solve([5, -7], [-7, 5])); // true
```

---

Solution 1:
```js
const solve = (arrOne, arrTwo) => {
  return arrOne.every(a => arrTwo.find(b => a === b));
};
```