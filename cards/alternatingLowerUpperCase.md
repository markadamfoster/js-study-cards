You are given an array of lowercase single string characters as an argument. Return the same array but with each character alternating lowercase, then uppercase.

## Example
```js
solve(['a', 'b', 'c', 'd', 'e']) // ['a', 'B', 'c', 'D', 'e']
```

## Setup
```js
const solve = (strArray) => {
  return;
};

console.log(solve(['a', 'b', 'c', 'd', 'e'])) // ['a', 'B', 'c', 'D', 'e']
```

---

```js
const solve = (strArray) => {
  return strArray.map((char, i) => {
    return i % 2 === 0 ? char.toLowerCase() : char.toUpperCase();
  });
};
```