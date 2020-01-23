You are given an array containing multiple single word strings as an argument. Return true if they are all anagrams of each other.

An anagram is a word made by rearranging the letters of a different word, using all the letters exactly once.

Consider upper and lower case characters the same.

## Setup
```js
const solve = strArray => {
  return;
};

console.log(solve(["act", "cat", "tac"])); // true
console.log(solve(["act", "cat", "garden"])); // false
console.log(solve(["UPPERCASE", "praepuces"])); // true
```

---
```js
const solve = strArray => {
  return strArray
    .map(word =>
      word
        .toLowerCase()
        .split("")
        .sort()
        .join("")
    )
    .every((word, i, arr) => word === arr[0]);
};
```