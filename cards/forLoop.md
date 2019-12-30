```js
for (let i = 0; i < 5; i++) {
  setTimeout(function() { console.log(i); }, i * 1000 );
}
```

What will this code print?

---

It will print `0 1 2 3 4`, because we use `let` instead of `var` here. The variable `i` is only seen in the `for` loop’s block scope.