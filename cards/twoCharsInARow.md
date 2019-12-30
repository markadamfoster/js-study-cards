You are given a single word string as an argument. Return true if it contains two identical characters in a row, false if not.

### Setup & Examples
```js
const solve = strArg => {
  return;
};

console.log(solve("terrific")); // true
console.log(solve("cats")); // false
console.log(solve("cats!!")); // true
```

---

```js
const solve = strArg => {
  return strArg.split("").some((char, i) => {
    return char === strArg[i + 1];
  });
};
```