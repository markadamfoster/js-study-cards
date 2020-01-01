What does this code output?

```js
const obj1 = {
    value: 'hi',
    print: function() {
        console.log(this);
    },
};

new obj1.print(); // ?
```

---

print {}