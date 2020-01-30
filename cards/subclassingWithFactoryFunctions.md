# Subclassing with factory functions

Take the following code and implement a "paid user" subclass using the factory function approach.

Paid users should have the additional parameter of "accountBalance", and should be able to increment and get the account balance (along with the normal user functions).

## Starter Code

```js
const userFunctions = {
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

function userCreator(name, score) {
  const newUser = Object.create(userFunctions);
  newUser.name = name;
  newUser.score = score;
  return newUser;
}

const paidUser1 = paidUserCreator("Mark", 8, 25);
paidUser1.getScore(); // 8
paidUser1.getBalance(); // 25

paidUser1.increment();
paidUser1.incrementBalance();

paidUser1.getScore(); // 9
paidUser1.getBalance(); // 26
```

---

```js
const userFunctions = {
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

const paidUserFunctions = {
  incrementBalance: function() {
    this.accountBalance++;
  },
  getBalance: function() {
    console.log(this.accountBalance);
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

const paidUser1 = paidUserCreator("Mark", 8, 25);
paidUser1.getScore();
paidUser1.getBalance();

paidUser1.increment();
paidUser1.incrementBalance();

paidUser1.getScore();
paidUser1.getBalance();
```
