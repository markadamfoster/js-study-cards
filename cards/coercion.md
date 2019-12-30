What will the code below output to the console and why ?

```js
console.log(1 +  "2" + "2");
console.log(1 +  +"2" + "2");
console.log(1 +  -"1" + "2");
console.log(+"1" +  "1" + "2");
console.log( "A" - "B" + "2");
console.log( "A" - "B" + 2);
```

---

```js
console.log(1 +  "2" + "2"); // 122
console.log(1 +  +"2" + "2"); // 32
console.log(1 +  -"1" + "2"); // 02
console.log(+"1" +  "1" + "2"); // 112
console.log( "A" - "B" + "2"); // NaN2
console.log( "A" - "B" + 2); // NaN
```