What is hoisting? How does hoisting work for `var`, `let`, `const`, function declarations and function expressions?

---

Hoisting is when the JavaScript engine moves function and variable declarations "to the top" before the code is executed.

1. `var` is hoisted
2. `let` & `const` are not hoisted
3. for function declarations, the entire declaration is hoisted
4. for function expressions, only the variable declaration is hoisted, not the entire definition.