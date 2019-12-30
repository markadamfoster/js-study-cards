How do you add an element at the beginning of an array? How do you add one at the end? (show the ES5 way, as well as a new way only possible with ES6)

---

### ES5:
```js
const myArray = [2, 3, 4];

myArray.push('at end');
myArray.unshift('at beginning');
```

### ES6:
```js
const myArray = [ 1, 2, 3 ];
const newArray = ['at beginning', ...myArray, 'at end'];
```