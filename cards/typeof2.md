What is the value of `typeof undefined == typeof NULL`?

---

`true`

1. JavaScript is case sensitive... so `NULL` is not `null`... in this case `NULL` is just a variable (that hasn't been defined). 

2. So with that in mind... it's comparing the type of `undefined` with an undefined variable... so it evaluates to `true`.

3. Note: if instead it was `typeof null`, that would be 'object' (`null` is a type of object)