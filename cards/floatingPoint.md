What will the code below output? Explain your answer.

```js
console.log(0.1 + 0.2);
console.log(0.1 + 0.2 == 0.3);
```

---

“I can’t be sure. It might print out 0.3 and true, or it might not. Numbers in JavaScript are all treated with floating point precision, and as such, may not always yield the expected results."

In reality, here is the output:

```js
console.log(0.1 + 0.2); // 0.30000000000000004
console.log(0.1 + 0.2 == 0.3); // false
```

