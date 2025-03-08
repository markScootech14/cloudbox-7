Several ways exist to sum all elements in a JavaScript array. Here are three common approaches:

1. Using a `for` loop:

This is a straightforward and efficient approach, especially for large arrays.

```javascript
function sumArrayForLoop(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}

let numbers = [1, 2, 3, 4, 5];
let sum = sumArrayForLoop(numbers);
console.log("Sum using for loop:", sum); // Output: Sum using for loop: 15
```

2. Using `reduce()`:

The `reduce()` method is a more functional approach and can be more concise.  It's generally considered more readable for this specific task.

```javascript
function sumArrayReduce(arr) {
  return arr.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
}

let numbers2 = [10, 20, 30, 40, 50];
let sum2 = sumArrayReduce(numbers2);
console.log("Sum using reduce:", sum2); // Output: Sum using reduce: 150
```

3. Using `forEach()`:

While `forEach()` isn't designed specifically for summing, it can be used.  However, it's less efficient and less readable than `reduce()` for this purpose.  This example demonstrates it for completeness but `reduce()` is preferred.

```javascript
function sumArrayForEach(arr) {
  let sum = 0;
  arr.forEach(number => sum += number);
  return sum;
}

let numbers3 = [1, 2, 3, 4, 5, 6];
let sum3 = sumArrayForEach(numbers3);
console.log("Sum using forEach:", sum3); // Output: Sum using forEach: 21

```

The `reduce()` method is generally preferred for its readability and conciseness when summing array elements in JavaScript.  The `for` loop is a good alternative if performance is absolutely critical in very specific scenarios (though the difference is often negligible unless dealing with extremely large arrays). Avoid `forEach()` for this specific task.
