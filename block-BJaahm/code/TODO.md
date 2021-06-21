1. Construct a function intersection that compares input arrays and returns a new array with elements found in all of the inputs. You can only use reduce method to do this.

```js
function intersection(...arrays) {
  let first = arrays[0];
  for (let i = 1; i < arrays.length; i++) {
    let next = arrays[0];
    first.filter((elem) => next.includes(elem));
  }
  return first;
}

// Test
console.log(
  intersection([5, 10, 15, 20], [15, 88, 1, 5, 7], [1, 10, 15, 5, 20])
); // should log: [5, 15]
```

2. Construct a function `union` that compares input arrays and returns a new array that contains all elements. If there are duplicate elements, only add it once to the new array. Preserve the order of the elements starting from the first element of the first input array. You can only use reduce method to do this.

```js
function union(...arrays) {
  let first = arrays[0];
  for (let i = 1; i < arrays.length; i++) {
    let next = arrays[i];
    first.filter((elem) => !next.includes(elem));
    first = first.concat(next);
  }
}

// Test
console.log(union([5, 10, 15], [15, 88, 1, 5, 7], [100, 15, 10, 1, 5]));
// should log: [5, 10, 15, 88, 1, 7, 100]
```