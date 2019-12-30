What will this code print out?

```js
const obj = {
    arr: []
};
 
obj.arr.push(17);
 
console.log(obj.arr === [17]);
```

---

`false`. For reference-type values in JavaScript, the equality operator checks if the references are pointing to the same item in memory (it does not check the **contents** of that item).