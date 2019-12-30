Write 3 different functions that accept a string and return that string in reverse.

## Setup

```js
const rev1 = str => {
  return str;
};

const rev2 = str => {
  return str;
};

const rev3 = str => {
  return str;
};

console.log(rev1("hello world"));
console.log(rev2("hello world"));
console.log(rev3("hello world"));
```

---

### Option 1:
Using the `array.reverse()` method
```js
function reverse (str) {
  return str.split('').reverse().join('');
} 
```

### Option 2:
Using a `for...of` loop
```js
function reverse(str) {
  let reversed = '';

  for (let character of str) {
    reversed = character + reversed;
  }
  return reversed;
}
```

### Option 3:
```js
function reverse(str) {
  return str.split('').reduce((result, char) => {
    return char + result
  }, '')
}
```

### Option 4:
```js
function reverse(str) {
  let reversed = [];
  str.split("").forEach(char => {
    reversed.unshift(char);
  });
  return reversed.join("");
}
```