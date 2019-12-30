Demonstrate (using code) the 4 "rules" around invoking a function with the `new` keyword.

---

```js
/* 
1. the function creates a new object and binds it to the `this` keyword
*/

function DemoConstructor1() {
  // we don't do anything with `this` here, but it still logs an empty object.
  console.log(this); // DemoConstructor1 {}
}
const demo1 = new DemoConstructor1();

/*
2. sets the object's `__proto__` to be the prototype of the constructor
*/

function DemoConstructor2() {}
const demo2 = new DemoConstructor2();
console.log(demo2.__proto__ === DemoConstructor2.prototype); // true

/*
3. If you try to return something other than an array, object or function,
it ignores your return and instead returns `this`
*/
function DemoConstructor3() {
  this.whatever = "hi";
  return 10; // it still returns here, but returns `this`
  console.log("I'm never ran");
}
const demo3 = new DemoConstructor3();
console.log(demo3); // DemoConstructor3 { whatever: 'hi' }

// 4. If there's no explicit return, it returns `this` at the end of the function
function DemoConstructor4() {
  this.whatever = "hi lol";
  // notice... no explicit return
}
const demo4 = new DemoConstructor4();
console.log(demo4); // DemoConstructor4 { whatever: 'hi lol' }

```