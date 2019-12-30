# Duplicate a string to fill an array

## Problem:
You are given a string and an integer K as arguments. Return an array of strings that is K elements long, where each element is the string that was provided.

## Example:
```js
solve("abc", 5) // ["abc", "abc", "abc", "abc", "abc"]

solve("Hi!", 3) // ["Hi!", "Hi!", "Hi!"]
```

## Setup:
```js
const solve = (strArg, k) => {
  return;
};

console.log(solve("abc", 5)); // ["abc", "abc", "abc", "abc", "abc"]
```

---

```js
const solve = (strArg, k) => {
  return Array(k).fill(strArg);
};
```