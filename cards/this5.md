What does this code output?

```js
const obj = {
    value: 'hi',
    printThis: function() {
        console.log(this);
    }
};

const print = obj.printThis;
obj.printThis(); // ?
print(); // ?
```

---

```js
{ value: 'hi', printThis: [Function: printThis] }
```
the global `window` object
