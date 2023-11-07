# Array Method: forEach

- Is a built-in JavaScript array method that allows you to iterate over the elements of an array and perform a specified action for each element. It is a higher-order function, which means it takes a callback function as its argument.

  The syntax for using forEach is as follows:

  ```javascript
  array.forEach(callback(element, index, array), thisArg);
  ```

  Here's what each part of the syntax means:

  - **`callback`**: This is a function that will be called once for each element in the array. It can take up to three arguments:
    - `element`: The current element being processed in the array.
    - `index`: The index of the current element being processed.
    - `array`: The array forEach was called upon.
  - `thisArg` (optional): An object to which the `this` keyword refers inside the `callback` function. If not provided, `this` will refer to the global object (in non-strict mode) or undefined (in strict mode).

- Here's an example of how you might use forEach to iterate over an array:

  ```javascript
  const numbers = [1, 2, 3, 4, 5];

  numbers.forEach(function (element, index, array) {
    console.log(`Element at index ${index} is: ${element}`);
  });
  ```

  This will output:

  ```
  Element at index 0 is: 1
  Element at index 1 is: 2
  Element at index 2 is: 3
  Element at index 3 is: 4
  Element at index 4 is: 5
  ```

- **`KEEP IN MIND`** that forEach does not modify the original array and always returns undefined. If you want to modify the array or return a new array based on the original, you might want to consider using methods like map, filter, or reduce.

- Also, it's worth noting that you can use arrow functions for the callback in ES6+ for a more concise syntax:

  ```javascript
  const numbers = [1, 2, 3, 4, 5];

  numbers.forEach((element, index) => {
    console.log(`Element at index ${index} is: ${element}`);
  });
  ```

  This achieves the same result as the previous example.
