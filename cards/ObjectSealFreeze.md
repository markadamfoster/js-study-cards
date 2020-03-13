Describe what the Object.seal() and Object.freeze() methods do.

---

Both of these methods have to do with controlling how if/how changes can be made to an object. This is particularly useful with functional programming, where we take special care to limit side effects and mutating data.

## Object.seal()
You seal an object by passing it into the `Object.seal` method,  like this:
```js
Object.seal(myObject);
```

Once an object is sealed, you can update existing values, but deleting and adding new properties does not work: 

- ✅ updating properties still works
- ❌ deleting properties does NOT work
- ❌ adding new properties does NOT work

```js
const user1 = {
  firstName: “Mark”,
  lastName: "Foster”
};

Object.seal(user1); // 🛡 SEAL IT!

user1.firstName = “Ignatius”; // ✅ updating existing values still works
delete user1.lastName; // ❌ deleting properties does NOT work
user1.email = “ted@example.com”; // ❌ adding new properties does NOT work

console.log(user1); // { firstName: ‘Ignatius’, lastName: ‘Foster’ }
```

## Object.freeze()
You freeze an object by passing it into the `Object.freeze` method,  like this:
```js
Object.freeze(myObject);
```

Once an object has been frozen, you can no longer update, add, or delete properties:

- ❌ updating properties does NOT work
- ❌ deleting properties does NOT work
- ❌ adding new properties does NOT work

```js
const user1 = {
  firstName: “Mark”,
  lastName: "Foster”
};

Object.freeze(user1); // 🥶 FREEZE IT!

user1.firstName = “Ignatius”; // ❌ updating values does NOT work
delete user1.lastName; // ❌ deleting properties does NOT work
user1.email = “ted@example.com”; // ❌ adding new properties does NOT work

console.log(user1); // { firstName: ‘Mark’, lastName: ‘Foster’ }

```