---
title: Partition Array
description: Splits an array into two arrays based on a callback function.
author: Swaraj-Singh-30
tags: javascript,array,partition,reduce,utility
---

```js
const partition = (arr, callback) =>
  arr.reduce(
    ([pass, fail], elem) => (callback(elem) ? [[...pass, elem], fail] : [pass, [...fail, elem]]),
    [[], []]
  );

// Usage:
const numbers = [1, 2, 3, 4, 5, 6];
const isEven = (n) => n % 2 === 0;
console.log(partition(numbers, isEven)); // Output: [[2, 4, 6], [1, 3, 5]]
```