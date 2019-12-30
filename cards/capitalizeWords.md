Write a function that accepts a string.  The function should capitalize the first letter of each word in the string then return the capitalized string.

## Setup
```js
const capitalize = str => {
  return;
};

console.log(capitalize("a short sentence")); // 'A Short Sentence'
console.log(capitalize("a lazy fox")); // 'A Lazy Fox'
console.log(capitalize("look, it is working!")); // 'Look, It Is Working!'

```

---

```js
function capitalize(str) {
  return str.split(" ").map(word => {
    return word[0].toUpperCase() + word.slice(1)
  }).join(" ")
}
```