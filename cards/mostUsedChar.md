Write a function that accepts a string and returns the character contained most often in that string.

For example, given the string "abbbc" it would return "b".

## Setup

```js
const solve = str => {
  return;
};

console.log(solve("abbc")); // b
console.log(solve("abbcccc")); // c
```

---

```js
function maxChar(str) {
  const charMap = str.split('').reduce((result, char) => {
    result[char] ? result[char]++ : result[char] = 1
    return result
  }, {})

  let max = 0;
  let maxChar = ''

  for (let char in charMap) {
    if (charMap[char] > max) {
      max = charMap[char]
      maxChar = char
    }
  }

  return maxChar
}
```