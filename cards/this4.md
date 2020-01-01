What does this code output?

```js
function fn() {
  console.log(this);
}

fn(); // ?
```

---

This logs out the global object (`window` in a browser)