# How to create function expressions?

- function expressions are a way to define a function as a value and assign it to a variable.

- This allows you to create anonymous functions (functions without a name) or give them a name if desired.

  Here's an example of a function expression:

  ```javascript
  const add = function (x, y) {
    return x + y;
  };

  console.log(add(2, 3));
  ```

  In this example, add is a variable that holds a function. This function takes two parameters (x and y) and returns their sum. The function doesn't have a name, but it's assigned to the variable add, so you can call it using add(2, 3).

- Function expressions are often used in cases where you want to pass a function as an argument to another function, or when you want to assign a function to a variable based on certain conditions.
