# Call Stack or Function Execution Stack

- The call stack, also known as the execution stack or function execution stack, is a crucial concept in JavaScript. It keeps track of the functions that are currently being executed by the JavaScript engine.

- When a script starts running, the JavaScript engine creates a global execution context and pushes it onto the call stack. As functions are called, new execution contexts are created for each function and pushed onto the stack. When a function finishes executing, its execution context is popped off the stack, and the program continues with the next item on the stack.

- Here's an example to illustrate how the call stack works:

  ```javascript
  function add(x, y) {
    return x + y;
  }

  function multiply(a, b) {
    return a * b;
  }

  function square(n) {
    return multiply(n, n);
  }

  let result = square(add(2, 3));
  console.log(result);
  ```

  1. When the script starts, a global execution context is created and pushed onto the call stack.
  2. The code encounters the let result = square(add(2, 3)); line. It first calls the add function with arguments 2 and 3.
     - The add function is pushed onto the call stack with its own execution context.
     - The add function returns 5 and is then popped off the stack.
  3. The returned value 5 is passed as an argument to the square function.
     - The square function is pushed onto the stack with its own execution context.
     - Inside square, it calls the multiply function.
  4. The multiply function is pushed onto the stack with its own execution context.
     - Inside multiply, it returns the product of the two arguments (n \* n).
     - The multiply function returns the result.
  5. The multiply function is popped off the stack, and the result is returned to the square function.
  6. The square function finishes executing and is popped off the stack. The result is returned to the main code.
  7. Finally, the main code assigns the result to the variable result and logs it to the console.

- The call stack ensures that functions are executed in the correct order and that the program doesn't lose track of its state. If the stack grows too large (due to too many nested function calls), it can lead to a stack overflow error.
