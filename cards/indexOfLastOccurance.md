You are given an array of integers and an integer K as arguments. Return the index of the last occurrence of integer K in the array. Argument Integer K is guaranteed to be found in the array at least once.

**Examples**
```js
solve([4, 1, 3, 5, 3, 4, 2], 4); // 5
solve([-1, -1, 3, 5, 3, 2], -1); // 1
```

**Setup**
```js
const solve = (intArray, k) => {
  return;
};

console.log(solve([4, 1, 3, 5, 3, 4, 2], 4)); // 5
console.log(solve([-1, -1, 3, 5, 3, 2], -1)); // 1
```

---

```js
const solve = (intArray, k) => {
  return intArray.lastIndexOf(k);
};

console.log(solve([4, 1, 3, 5, 3, 4, 2], 4)); // 5
console.log(solve([-1, -1, 3, 5, 3, 2], -1)); // 1
```