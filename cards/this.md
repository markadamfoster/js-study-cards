What does this output (and why)?

```js
var myObject = {
  foo: "bar",
  func: function() {
      var self = this;
      console.log("outer func:  this.foo = " + this.foo);
      console.log("outer func:  self.foo = " + self.foo);
      (function() {
          console.log("inner func:  this.foo = " + this.foo);
          console.log("inner func:  self.foo = " + self.foo);
      }());
  }
};

myObject.func();
```

---

outer func:  this.foo = bar
outer func:  self.foo = bar
inner func:  this.foo = undefined
inner func:  self.foo = bar

In the outer function, `this` and `self` both refer to `myObject`, and can thus access `foo`
In the inner function, `self.foo` is still in scope, but `this` no longer references `myObject`, so `this.foo` is undefined