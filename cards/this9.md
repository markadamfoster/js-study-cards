What does this code output (and why)?

```js
const obj = {
  printVal: "Print value",
  generatePrintFn: function() {
    return function() {
      console.log(this.printVal);
    };
  }
};

const print = obj.generatePrintFn();
print(); // ?
```

---

`undefined`

This is because the inner, returned function is a free function invocation. Therefore `this` refers to the global object, which does not have a `printVal` property.
