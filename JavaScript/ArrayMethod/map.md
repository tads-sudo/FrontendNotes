# Array Method: Map

- Is a higher-order function in JavaScript that is used to apply a given function to each element of an array and returns a new array with the results. It doesn't modify the original array; instead, it creates a new one.

  The basic syntax for using the map method is as follows:

  ```javascript
  let newArray = originalArray.map(callback(element, index, array));
  ```

  Here's what each part of the syntax means:

  - **`originalArray`**: The array you want to apply the map function on.

  - **`callback`**: This is the function that will be called for each element in the array. It can take up to three arguments:
    - **`element`**: The current element being processed in the array.
    - **`index`** (optional): The index of the current element being processed.
    - **`array`** (optional): The array map was called upon.

- Here's an example of using map to double each element in an array:

  ```javascript
  let numbers = [1, 2, 3, 4, 5];

  let doubledNumbers = numbers.map(function (num) {
    return num * 2;
  });

  // doubledNumbers will be [2, 4, 6, 8, 10]
  ```

  You can also use arrow functions for brevity:

  ```javascript
  let doubledNumbers = numbers.map((num) => num * 2);
  ```
