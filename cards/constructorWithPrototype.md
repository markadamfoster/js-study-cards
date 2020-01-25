Write a `UserCreator` constructor function that creates a user object. It should have parameters of `name` and `score`. 

Use the prototype feature to give the ability to increment, decrement, and get a user's score, without having those functions duplicated across all users.

---

```js
function User(name, score) {
  this.name = name;
  this.score = score;
}

User.prototype.increment = function() {
  this.score++;
};

User.prototype.decrement = function() {
  this.score--;
};

User.prototype.getScore = function() {
  console.log(this.score);
};

const user1 = new User("Mark", 10);

user1.getScore(); // 10
user1.increment();
user1.getScore(); // 11
user1.decrement();
user1.getScore(); // 10

```