You are given an array of integers and an integer K as arguments. Return the product of every integer in the array _except_ for K.

K is guaranteed to always be present in the argument array.

## Setup

```js
const solve = (intArray, k) => {
  return;
};

console.log(solve([1, 2, 3, 4, 5], 3)); // 40
```

---

```js
const solve = (intArray, k) => {
  return intArray
    .filter(n => n !== k)
    .reduce((total, int) => {
      return total * int;
    }, 1);
};
```