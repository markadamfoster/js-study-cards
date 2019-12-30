What is notable about the `apply`, `call`, and `bind` methods?

Demonstrate this in a code example for each.

---

These are all ways to explicity set the value of `this`.

```js
function log(arg1, arg2) {
  console.log(this);
  console.log("arg1:", arg1);
  console.log("arg2:", arg2);
}

const obj = {
  hello: "world"
};

// normal (no change to `this`)
log("one", "two"); // logs the global window/node object

// set `this` via call()
log.call(obj, "one", "two"); // { hello: 'world' }, one, two

// set `this` via apply()
log.apply(obj, ["one", "two"]); // { hello: 'world' }, one, two

// set `this` via bind()
const logBound = log.bind(obj, "one", "two");
logBound(); // { hello: 'world' }, one, two
```
