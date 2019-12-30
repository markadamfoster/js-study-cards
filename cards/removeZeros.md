# Remove the zeros from an array
You are given an array of integers containing some zeros as an argument. Return an array of integers with all zeros removed, while maintaining the original order.

## Example
```js
solve([0, 0, 2, 0, 3, 0, 5]); // [2, 3, 5]
```

## Setup
```js
const solve = intArray => {
  return;
};

console.log(solve([0, 0, 2, 0, 3, 0, 5])); // [2, 3, 5]
```

---

```js
const solve = intArray => {
  return intArray.filter(n => n);
};
```