Demonstrate 2 ways to clone an object. What is a potential pitfall with these? What is a workaround for that pitfall?

---

### Option 1: `Object.assign()`

```js
const clone = Object.assign({}, obj)
```

### Option 2: object spread

```js
const clone = { ...obj }
```

### Potential pitfall
These are only "shallow clones". If the original object contains a nested object, it is still a reference value.

### Workarounds
1. Utility libraries usually have a "deep clone" method
2. Poor man's workaround using `JSON.parse()` & `JSON.stringify()`:

```js
const deepClone = JSON.parse(JSON.stringify(obj))
```