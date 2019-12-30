Explain the `new` keyword in JavaScript.

---

The `new` keyword is a central part of OOP.

It is a way to invoke a function that adds some special behavior:

1. creates a new object and binds it to the `this` keyword
2. sets the object's `__proto__` to be the `prototype` of the constructing function. 
3. if there is a return other than an object, array, or function, it ignores that and returns `this` anyway
4. if there's no other return, it returns `this` at the end of the function

Functions that are meant to be invoked with the `new` keyword are known as "constructors".