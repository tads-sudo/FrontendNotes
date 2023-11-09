# Recursion

- Recursion in JavaScript is a programming technique where a function calls itself in order to solve a problem. This can be a powerful and elegant way to solve certain types of problems, especially those that can be broken down into smaller, similar subproblems.

- Here's an example of a simple recursive function in JavaScript that calculates the factorial of a non-negative integer:

  ```javascript
  function factorial(n) {
    if (n === 0) {
      return 1;
    } else {
      return n * factorial(n - 1);
    }
  }
  ```

  In this example, factorial is a function that calculates the factorial of a non-negative integer n. The base case is when n is 0, in which case the function returns 1. Otherwise, it recursively calls itself with n - 1 and multiplies the result by n.

  It's important to have a base case in a recursive function to prevent it from calling itself indefinitely (which would lead to a stack overflow). The base case provides a termination condition for the recursion.

  Here's an example of how you might use the factorial function:

  ```javascript
  let result = factorial(5); // Calculates 5!
  console.log(result); // Output: 120
  ```

- **`KEEP IN MIND`** that recursion can be less efficient than iterative approaches for some problems, as it involves function calls and can lead to a large number of function calls on the call stack. However, for certain types of problems, recursion can be a very elegant and natural solution.
