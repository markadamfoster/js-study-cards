Write 2 functions that return a boolean indicating whether or not a string is a palindrome.

1. The shortest & simplest way
2. An alternate way

**Setup**
```js
const solve = str => {
  return;
}

console.log(solve("abba")); // true
console.log(solve("racecar!")); // false
console.log(solve("ab ba")); // true
console.log(solve("race car")); // false
```

---

### Shortest & Simplest
```js
function isPalindrome(str) {
  return (str == str.split('').reverse().join(''));
}
```

### Alternate
```js
function palindrome(str) {
  return str.split('').every((char, i) => {
    return char === str[str.length - i - 1];
  })
}
```
Note: one issue here is that it does twice as much checking as needed. You could add an escape hatch once you're 1/2 through.