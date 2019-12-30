What is a "constructor" in JavaScript? Include a code example.

---

A constructor is a functions that is meant to be invoked with the `new` keyword (this is a part of OOP)

```js
function PersonConstructor(name, age) {
  this.name = name;
  this.age = age;
}

const mark2 = new PersonConstructor("mark", 35);
console.log("mark2:", mark2);
```