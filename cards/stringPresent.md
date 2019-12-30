You are given an array of strings and a single string as arguments. Return true if the single string is also present in the array.

*Examples*
```js
solve(['apple', 'orange', 'banana'], 'orange'); // true
solve(['apple', 'orange', 'banana'], 'pear'); // false
```

*Setup*
```js
const solve = (strArray, strArg) => {
  return;
};

console.log(solve(["apple", "orange", "banana"], "orange")); // true
console.log(solve(["apple", "orange", "banana"], "pear")); // false
```
---
```js
const solve = (strArray, strArg) => {
  return strArray.includes(strArg);
};
```
