You are given a string and integer K as arguments. Return the Kth most frequently occurring character.

## Setup
```js
const solve = (strArg, k) => {
  return;
};

console.log(solve("aaabbc", 2)); // b
console.log(solve("bbbbxyyzzz", 3)); // y
```

---

```js
const solve = (strArg, k) => {
  const charMap = strArg.split("").reduce((map, char) => {
    map[char] = map[char] + 1 || 1;
    return map;
  }, {});

  return Object.keys(charMap)
    .map(char => {
      return [char, charMap[char]];
    })
    .sort((a, b) => {
      a[1] - b[1];
    })[k - 1][0];
};
```