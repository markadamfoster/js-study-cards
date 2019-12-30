You are given two single word strings as arguments. Return true if the second string is a prefix of the first.

```js
solve("banner", "bang") // false
solve("hugging", "hug") // true
```

### Setup
```js
const solve = (str1, str2) => {
  return;
};

console.log(solve("banner", "bang")); // false
console.log(solve("hugging", "hug")); // true
```

---

```js
const solve = (strOne, strTwo) => {
  return strOne.startsWith(strTwo);
};
```