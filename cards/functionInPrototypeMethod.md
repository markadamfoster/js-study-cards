This code doesn't work. Why not, and how can you fix it?

```js
function User(name, score) {
  this.name = name;
  this.score = score;
}

User.prototype.increment = function() {
  function add1() {
    this.score++;
  }
  add1();
};

const user1 = new User("Mark", 10);

user1.increment();
```

---

The above code doesn't work because the `this` in the `add1` function doesn't refer to `user1`. This is a free function invocation, so `this` refers to the global object.

One way to fix this would be to use an arrow function instead:

```js
User.prototype.increment = function() {
  const add1 = () => this.score++;
  add1();
};
```
