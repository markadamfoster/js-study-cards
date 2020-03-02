## A "userCreator" using the factory function approach

Using the OOP "factory function approach", create a `userCreator` and `paidUserCreator` functions (with the following parameters and methods). Note: the method declaration/code should not be duplicated across all users.

### `userCreator`

Parameters:

- `name`
- `score`

Methods:

- `sayName`
- `incrementScore`
- `getScore`

### `paidUserCreator`

Parameters:

- same as `userCreator`
- `balance`

Methods:

- same methods as `userCreator`
- `getBalance`
- `incrementBalance`

## Setup:

```js
const user1 = userCreator("Mark", 10);
user1.sayName(); // Mark
user1.getScore(); // 10
user1.incrementScore();
user1.getScore(); // 11

const paidUser1 = paidUserCreator("Ted", 8, 25);
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
const userFunctions = {
  sayName: function() {
    console.log(this.name);
  },
  incrementScore: function() {
    this.score++;
  },
  getScore: function() {
    console.log(this.score);
  }
};

const paidUserFunctions = {
  getBalance: function() {
    console.log(this.accountBalance);
  },
  incrementBalance: function() {
    this.accountBalance++;
  }
};

function userCreator(name, score) {
  const newUser = Object.create(userFunctions);
  newUser.name = name;
  newUser.score = score;
  return newUser;
}

function paidUserCreator(name, score, accountBalance) {
  const newPaidUser = userCreator(name, score);
  Object.setPrototypeOf(newPaidUser, paidUserFunctions);
  newPaidUser.accountBalance = accountBalance;
  return newPaidUser;
}

Object.setPrototypeOf(paidUserFunctions, userFunctions);
```
