You are given an array of strings as an argument. Return a new array containing all elements from the original array excluding the first element.

## Example
```js
solve(["pears", "apples", "oranges"])// ["apples", "oranges"]
```

## Setup
```js
const solve = (strArray) => {
  return;
};

console.log(solve(["pears", "apples", "oranges"])) // ["apples", "oranges"]
```

---

```js
const solve = (strArray) => {
  return strArray.slice(1)
};
```