You are given an array of integers containing some zeros as an argument. Return a new array that contains all the elements of the original (in the same order), but with all of the zero values moved to the right hand side of the array.

## Setup

```js
const solve = intArray => {
  // solution here!
};

console.log(solve([0, 1, 0, 2, 0])); // [1, 2, 0, 0, 0]
console.log(solve([3, 0, 4, 0, 0, 1, 6, 0])); // [3, 4, 1, 6, 0, 0, 0, 0]
```

---

## Solution:

```js
const solve = intArray => {
  const zeros = intArray.filter(n => !n);
  const nonZeros = intArray.filter(n => n);
  return [...nonZeros, ...zeros];
};
```
