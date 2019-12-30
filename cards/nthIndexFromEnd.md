You are given an array of integers and an integer K as arguments. Return the element that is the Kth index from the end of the array.

Assume that the argument array length will always be at least K + 1

*Example:*
```js
solve([1,2,3,4,5,6], 0) // 6

solve([-1,2,3,-4,5,0], 3) // 3
```
*Setup*
```js
const solve = (intArray, k) => {
  return;
};

console.log(solve([1, 2, 3, 4, 5, 6], 0)); // 6
console.log(solve([-1, 2, 3, -4, 5, 0], 3)); // 3
```

---

```js
const solve = (intArray, k) => {
  return intArray[intArray.length - 1 - k];
};
```