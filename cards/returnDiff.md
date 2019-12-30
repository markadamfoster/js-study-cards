Consider the two functions below. Will they both return the same thing? Why or why not?

```js
function foo1()
{
  return {
      bar: "hello"
  };
}

function foo2()
{
  return
  {
      bar: "hello"
  };
}
```

---

```js
console.log(foo1()) // { bar: 'hello' }
console.log(foo2()) // undefined
```

In `foo2`, the `return` is on its own line. The function returns there, and never reaches the next line.