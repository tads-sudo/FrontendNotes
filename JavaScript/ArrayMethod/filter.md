# Array Method: Filter

- Is a built-in function in JavaScript that allows you to create a new array containing only the elements from an existing array that satisfy a certain condition. It does not modify the original array, but instead returns a new array with the filtered elements.

- Here is the basic syntax of the filter method:

  ```javascript
  let newArray = array.filter(callback(element[, index[, array]])[, thisArg])
  ```

  Here's what each part of the syntax means:

  - **`array`**: The original array you want to filter.
  - **`callback`**: A function that tests each element in the array. It takes three arguments:

    - `element`: The current element being processed in the array.
    - `index` (optional): The index of the current element.
    - `array` (optional): The array filter was called upon.
    - `thisArg` (optional): The value to be used as this when executing the callback function.

    The callback function should return true to include the element in the new array, or false to exclude it.

- Here's an example of how you might use the filter method to filter out even numbers from an array:

  ```javascript
  let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

  let evenNumbers = numbers.filter(function (number) {
    return number % 2 === 0;
  });

  console.log(evenNumbers); // Output: [2, 4, 6, 8, 10]
  ```

  In this example, the callback function checks if each number in the array is even by using the modulo operator (%). If the result is 0, it means the number is even and true is returned, so it gets included in the evenNumbers array.

- **`KEEP IN MIND`** that filter does not modify the original array; it returns a new array with the filtered elements.
