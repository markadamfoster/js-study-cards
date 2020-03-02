# User and PaidUser classes

Create a `User` class, with:

- parameters `name` and `score`
- methods `sayName`, `incrementScore`, `getScore`

Then, create a `PaidUser` subclass, with:

- same parameters & methods as the UserCreator class
- additional parameter of `balance`
- additional methods of `incrementBalance` and `getBalance`

After you're done, this code should work:

```js
const user1 = new User("Mark", 10);
user1.sayName(); // My name is Mark.
user1.getScore(); // Score: 10
user1.incrementScore();
user1.getScore(); // Score: 11

const paidUser1 = new PaidUser("Ted", 10, 25);
paidUser1.sayName(); // My name is Ted.
paidUser1.getScore(); // Score: 10
paidUser1.incrementScore();
paidUser1.getScore(); // Score: 11
paidUser1.getBalance(); // Balance: 25
paidUser1.incrementBalance();
paidUser1.getBalance(); // Balance: 26
```

---

```js
class User {
  constructor(name, score) {
    this.name = name;
    this.score = score;
  }

  sayName() {
    console.log(`My name is ${this.name}.`);
  }

  incrementScore() {
    this.score++;
  }

  getScore() {
    console.log("Score:", this.score);
  }
}

class PaidUser extends User {
  constructor(name, score, accountBalance) {
    super(name, score);
    this.accountBalance = accountBalance;
  }

  incrementBalance() {
    this.accountBalance++;
  }

  getBalance() {
    console.log("Balance:", this.accountBalance);
  }
}
```
