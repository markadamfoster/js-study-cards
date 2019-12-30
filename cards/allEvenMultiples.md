You are given an array of integers and an integer K as arguments. Return true if each integer is an even multiple of integer K.

**Examples**
```js
solve([2, 4, 6, 8], 2); // true
solve([12, 14, 36, 18], 9); // false
```
**Setup**
```js
const solve = (intArray, k) => {
  return;
};

console.log(solve([2, 4, 6, 8], 2)); // true
console.log(solve([12, 14, 36, 18], 9)); // false;
```

---

```js
const solve = (intArray, k) => {
  return intArray.every(int => int % k === 0);
};
```