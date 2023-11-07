# Array Method: Every

- The every method is used to check whether all elements in an array pass a particular test.

- It takes a callback function as an argument and applies it to each element in the array until the callback returns false for an element, or until all elements have been tested.

- The syntax for the every method is as follows:

  ```javascript
  array.every(callback(element[, index[, array]])[, thisArg])
  ```

  Here's what each part of the syntax means:

  - **`array`**: The array on which every is being called.

  - **`callback`**: A function that is called for each element in the array. It can take up to three arguments:
    - `element`: The current element being processed in the array.
    - `index` (optional): The index of the current element being processed.
    - `array` (optional): The array on which every was called.
    - `thisArg` (optional): Value to use as this when executing the callback.

- The `every` method returns true if the callback returns true for all elements in the array. If the callback returns false for at least one element, `every` returns false.

  Here's an example usage:

  ```javascript
  const numbers = [2, 4, 6, 8, 10];

  const allEven = numbers.every(function (number) {
    return number % 2 === 0;
  });

  console.log(allEven); // Output: true
  ```

  In this example, the callback function checks if each number in the array is even. Since all elements are even, every returns true.

  If, for example, one of the numbers was 7, then the callback would return false for that element, and every would return false overall.
