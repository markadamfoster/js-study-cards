# Find the number of vowels in a string

Write a function that returns the number of vowels used in a string.  Vowels are the characters 'a', 'e', 'i', 'o', and 'u'.

## Examples:
```js
function countVowels(str) {
  return;
}

console.log(countVowels("Hi There!")); // 3
console.log(countVowels("Icey Igloo")); // 5
console.log(countVowels("Why?")); // 0
```

---
Solution 1:
```js
function countVowels(str) {
  const VOWELS = ["a", "e", "i", "o", "u"];

  return str.split("").filter(char => VOWELS.includes(char.toLowerCase()))
    .length;
}
```

Solution 2:
```js
function countVowels(str) {
  const vowels = [ "a", "e", "i", "o", "u"]
  let count = 0

  for (let letter of str.toLowerCase()) {
    if (vowels.includes(letter)) count++
  }

  return count
}
```