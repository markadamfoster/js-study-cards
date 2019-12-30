Implement your own version of the `lastIndexOf()` array method.

## Setup
```js
const myLastIndexOf = (intArray, k) => {
  return;
};

console.log(myLastIndexOf([4, 1, 3, 5, 3, 4, 2], 4)); // 5
console.log(myLastIndexOf([-1, -1, 3, 5, 3, 2], -1)); // 1
```
---
```js
const myLastIndexOf = (intArray, k) => {
  for (let i = intArray.length - 1; i >= 0; i--) {
    if (intArray[i] === k) {
      return i;
    }
  }
};
```
