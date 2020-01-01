This code prints `undefined`. What are three ways we could "fix" that and instead have it print "Print value"?

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

```js
// Option 1: use bind()
const obj = {
    printVal: "Print value",
    generatePrintFn: function() {
        console.log(this.printVal);
    },
};

const print = obj.generatePrintFn.bind(obj);
print(); // "Print value"

// Option 2: use a `var self = this;` hack
const obj = {
    printVal: "Print value",
    generatePrintFn: function() {
        var self = this;
      
        return function print() {
            console.log(self.printVal);
        }
    },
};

const print = obj.generatePrintFn();
print(); // -> Print value

// Option 3: use an arrow fuction
const obj = {
    printVal: "Print value",
    generatePrintFn: function() {
        return () => console.log(this.printVal);
    },
};

const print = obj.generatePrintFn();
print(); // -> Print value
```