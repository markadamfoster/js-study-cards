Describe `Object.assign()` and demonstrate its use.

---

`Object.assign()` is used to assign properties from one object to another. 

- first param: the object that will receive properties
- all other params: the objects whose properties will be placed onto the first object.

Example:
```js
const hello = { hello: "world" };
const obj1 = { firstName: "Mark" };
const obj2 = { lastName: "Foster" };
const obj3 = { email: "mark@example.com" };

Object.assign(hello, obj1, obj2, obj3);

console.log("hello", hello);
// obj1: {
//   firstName: 'Mark',
//   lastName: 'Foster',
//   email: 'mark@example.com'
// }

const name = Object.assign({}, obj1, obj2);

console.log("name:", name);
// name: { firstName: 'Mark', lastName: 'Foster' }
```