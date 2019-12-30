Write 2 functions that create a "person" object (including a name and an age). 

Use:
1. a normal function declaration, and 
2. a constructor function

---

```js
// normal Function declaration
function personFn(name, age) {
  return {
    name,
    age
  };
}

const mark = personFn("Mark", 35);
console.log(mark);

// Constructor
function PersonConstructor(name, age) {
  this.name = name;
  this.age = age;
}

const mark2 = new PersonConstructor("mark", 35);
console.log("mark2:", mark2);
```