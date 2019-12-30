What is a potential pitfall with using `typeof bar === "object"` to determine if `bar` is an object? How can this pitfall be avoided?

---

The potential pitfall is that in JavaScript, `null` is also an object.

To avoid this pitfall, you'd need to also check explicitly for null:

```js
console.log((bar !== null) && (typeof bar === "object"));
```