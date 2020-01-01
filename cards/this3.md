What does this code output?

```js
const obj = {
  value: 5,
  printThis: function() {
    console.log(this);
  }
};

obj.printThis(); // ?
```
---

```js
{ value: 5, printThis: [Function: printThis] }
```
