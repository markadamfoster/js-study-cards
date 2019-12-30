Write a `reverseInt` function that takes an integer and returns the reverse of that integer.

## Setup
```js
const reverseInt = int => {
  return;
};

console.log(reverseInt(15)); // 51
console.log(reverseInt(981)); // 189
console.log(reverseInt(500)); // 5
console.log(reverseInt(-15)); // -51
console.log(reverseInt(-90)); // -9
```

---

```js
function reverseInt(n) {
  const reversed = n.toString().split('').reverse().join('')
  return parseInt(reversed) * Math.sign(n)
}
```