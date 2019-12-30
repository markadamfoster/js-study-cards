Illustrate the concept of "closure" with a simple code example of a counter, where the user can increment the count, but cannot otherwise change the count value. 

Explain why this concept is beneficial.

---

```js
function makeCounter() {
  let count = 0;

  return function() {
    count++;
    console.log(count);
  };
}

const counter = makeCounter();
counter(); // 1
counter(); // 2
counter(); // 3
```