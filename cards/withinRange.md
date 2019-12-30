You are given an array of integers and an array containing a range of integers (in the form of \[X, Y]) as arguments. Return an array containing all of the elements from the array of integers that are contained in the range.

X will always be a smaller number than Y.

There will always be at least one integer from the array found the X,Y range.

## Setup
```js
const solve = (intArray, range) => {
  return;
};

console.log(solve([1, 2, 3, 5, 6, 7], [2, 6])); // [3, 5]
console.log(solve([1, 2, 3, 4, 5, 10, 20], [4, 7])); // [5]

```

---

```js
const solve = (intArray, range) => {
  return intArray.filter(n => {
    return n > range[0] && n < range[1];
  });
};
```