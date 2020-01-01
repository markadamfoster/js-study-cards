What is `this` in JavaScript? What are the rules for how `this` is set?

---

`this` is a keyword in JavaScript, which generally refers to the object which an invoked function is a property of.

The exact value of `this` is determined by these 5 rules:

1. If the `new` keyword is used when calling the function, `this` inside the function is a brand new object created by the JavaScript engine.

2. If `apply`, `call`, or `bind` are used to call a function, `this` inside the function is the object that is passed in as the argument.

3. If a function is called as a method (i.e. dot notation is used), `this` is the object the function is a property of (i.e. the object to the left of the dot).

4. If a function is invoked as a free function invocation (none of the conditions above), `this` is the global object (In a browser this is `window`). _Note: Technically this is the same a rule 3a. These functions are methods on the global object._

5. If multiple rules apply, the rule highest on this list is used.

6. If using an arrow function, all these rules are ignored and it receives the `this` value of its surrounding scope. (i.e. what's the value of `this` on the line above the arrow function?)