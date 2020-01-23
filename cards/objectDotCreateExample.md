Create a `userCreator` function that creates a user object. It should accept `name` and `score` arguments. 

Use `Object.create` to give the ability to increment, decrement, and read a user's score, without having those functions duplicated across all users.

---

```js
function userCreator(name, score) {
  const newUser = Object.create(userFunctionStore);
  newUser.name = name;
  newUser.score = score;
  return newUser;
}

const userFunctionStore = {
  increment: function() {
    this.score++;
  },
  decrement: function() {
    this.score--;
  },
  getScore: function() {
    console.log(this.score);
  }
};

const user1 = userCreator("Mark", 10);
user1.getScore(); // 10
user1.increment(); 
user1.getScore(); // 11
user1.decrement(); 
user1.getScore(); // 10
```