You are given a lowercase string as an argument. Return true if each character in the string is shown an even number of times, false if not.

## Setup
```js
const solve = strArg => {
  return;
};

console.log(solve("aabbccdd")); // true
console.log(solve("abcdeffgg")); // false
```

---

```js
const solve = strArg => {
  const charMap = strArg.split("").reduce((map, char) => {
    map[char] ? map[char]++ : (map[char] = 1);
    return map;
  }, {});

  return Object.keys(charMap).every(char => {
    return charMap[char] % 2 === 0;
  });
};
```