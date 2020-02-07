You are given an array of integers containing some duplicates as an argument. Return the first element in the array that is duplicated twice.

## Setup
```js
const solve = intArray => {
  return;
};

console.log(solve([6, 2, 5, 1, 0, 12, 2])); // 2
console.log(solve([-6, 1, 5, -6, 0, -2, 3])); // -6
console.log(solve([3, 1, 5, 1, 0, -2, 3, 5])); // 1
```
---
```js
const solve = intArray => {
  const foundSoFar = [];
  let firstDupe = null;

  for (let i = 0; i < intArray.length; i++) {
    const char = intArray[i];
    if (foundSoFar.includes(char)) {
      firstDupe = char;
      break;
    } else {
      foundSoFar.push(char);
    }
  }

  return firstDupe;
};
```