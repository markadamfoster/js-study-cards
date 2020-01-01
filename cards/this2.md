What does this code output?

```js
function ConstructorExample() {
  console.log(this); // ?
  this.value = 10;
  console.log(this); // ?
}
new ConstructorExample();
```

---
```js
ConstructorExample {}
ConstructorExample { value: 10 }
```