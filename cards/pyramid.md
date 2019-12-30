# Printing a Pyramid

Write a function that accepts a positive number N. The function should console log a pyramid shape with N levels using the # character.  Make sure the pyramid has spaces on both the left *and* right hand sides

## Examples:
```js
pyramid(1)
// '#'
pyramid(2)
// '_#_'
// '###'
pyramid(3)
// '__#__'
// '_###_'
// '#####'
pyramid(4)
// '___#___'
// '__###__'
// '_#####_'
// '#######'
```

---

Video: https://www.udemy.com/coding-interview-bootcamp-algorithms-and-data-structure/learn/lecture/8546990#overview

```js
function pyramid(n) {
  const midpoint = Math.floor((2*n - 1) / 2)  

  for (let row = 0; row < n; row++) {
    let level = ""

    for (let col = 0; col < n*2-1; col++) {
      if (midpoint - row <= col && midpoint + row >= col) {
        level += "#"
      } else {
        level += "_"
      }
    }

    console.log(level);
  }
}
```
