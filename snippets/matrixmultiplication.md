---
title: Matrix Multiplication
tags: array, math
expertise: beginner
firstSeen: 2022-11-27T05:00:00-04:00
---

Calculates the `Multiplication` of two matrices.

- Use `Array.prototype.map()` to iterate over the elements in the matrices.
- Use `Array.prototype.reduce()` to calculate the summed up value for each element in the result matrix.

```js
const matrixMultiplication = (first, second) => {
  return first.map((rowFirst) =>
    second[0].map((_, item) =>
      rowFirst.reduce((accumulator, currentF, index) => accumulator + currentF * second[index][item], 0)
      )
    );
  }   
```

```js
const o_mat = [[10, 2, 1], [6, 2, 7]];
const s_mat = [[3, 6], [4, 3], [9, 1]];
matrixMultiplication(o_mat, s_mat); // [[47, 67], [89, 49]]
```
