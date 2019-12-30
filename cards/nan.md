What is `NaN`? What is its type? How can you reliably test if a value is equal to `NaN`?

---

`NaN` is a value that is "not a number". 

Its type is Number.

There are two ways to test if a value is equal to `NaN`. There is a global function `isNaN()` which is somewhat reliable, and a new ES6 function `Number.isNaN()` that is more reliable.