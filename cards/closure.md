What is a “closure” in JavaScript?

How is a closure created?

What is unique about a closure (in terms of what it gives you access to)?

---

A closure is the combination of a function and its lexical environment.

A closure is created every time a function is created, at function creation time.

A closure gives you access to an outer function's scope from within an inner function (even if the outer function is finished running).