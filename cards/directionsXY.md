You are given an array containing strings of directions (up, down, left, right) as an argument. Imagine a person standing on a grid at point 0, 0. For each direction in the array of strings, move your person in that direction on the grid. Return the final X,Y point that the person is standing at as an array of two integers.

## Setup
```js
const solve = directions => {
  return;
};

console.log(solve(["up", "up", "down", "left", "left", "right", "up"])); // [-1, 2]
```

---

```js
const solve = directions => {
  return directions.reduce(
    (position, direction) => {
      switch (direction) {
        case "up":
          return [position[0], position[1] + 1];
        case "down":
          return [position[0], position[1] - 1];
        case "left":
          return [position[0] - 1, position[1]];
        case "right":
          return [position[0] + 1, position[1]];
      }
    },
    [0, 0]
  );
};
```