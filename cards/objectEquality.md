What does the following code output (and explain why)

```js
const obj1 = { name: "Mark" }
const obj2 = { name: "Mark" }

console.log(obj1 === obj2)
```

---

This would be `false`.

For reference-type values, the equality operater only checks if the references are pointing to the same item. It doesn't check the properties/contents of the item itself.