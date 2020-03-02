# A User and PaidUser using the `new` keyword

Using the OOP `new` keyword approach, create `User` and `PaidUser` constructor functions (with the following parameters and methods).

### `User`

Parameters:

- `name`
- `score`

Methods:

- `sayName`
- `incrementScore`
- `getScore`

### `PaidUser`

Parameters:

- same as `User`
- `balance`

Methods:

- same methods as `User`
- `getBalance`
- `incrementBalance`

## Setup

```js
const user1 = new User("Mark", 10);
user1.sayName(); // Mark
user1.getScore(); // 10
user1.incrementScore();
user1.getScore(); // 11

const paidUser1 = new PaidUser("Ted", 8, 25);
paidUser1.sayName(); // Ted
paidUser1.getScore(); // 8
paidUser1.incrementScore();
paidUser1.getScore(); // 9

paidUser1.getBalance(); // 25
paidUser1.incrementBalance();
paidUser1.getBalance(); // 26
```

---

```js
function User(name, score) {
  this.name = name;
  this.score = score;
}

User.prototype.sayName = function() {
  console.log(this.name);
};

User.prototype.incrementScore = function() {
  this.score++;
};

User.prototype.getScore = function() {
  console.log(this.score);
};

function PaidUser(name, score, balance) {
  User.call(this, name, score);
  this.balance = balance;
}

PaidUser.prototype = Object.create(User.prototype);

PaidUser.prototype.getBalance = function() {
  console.log(this.balance);
};

PaidUser.prototype.incrementBalance = function() {
  this.balance++;
};
```
