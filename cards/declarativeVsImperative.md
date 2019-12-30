What is the difference between "declarative" and "imperative" code, and illustrate with an example.

---

Declarative code "declares the outcome" (the what & why), rather than the "how". Generally speaking, code that is more declarative communicates better.

For instance, using the spread operator:

```js
const myProps = { ...props }
```

is more declarative (and communicative) than a more imperative:

```js
 Array.apply(/* code stuff */)
```

We aren't as concerned as to *how* it works, as we are interested in the final outcome. More of the inner workings is abstracted away.