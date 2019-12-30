Illustrate the concept of closure by writing a simple code example of a counter where the user can increment, decrement, and read the count value, but can't do anything else.

---

```js
function makeCounter() {
  let count = 0;

  return {
    plus: () => count++,
    minus: () => count--,
    get: () => console.log(count)
  };
}
```