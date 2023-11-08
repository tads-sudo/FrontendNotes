# How to create a basic function?

- Creating a function in JavaScript is relatively straightforward.

- Functions in JavaScript are blocks of reusable code that can be called with a specific name.

- Here's the basic syntax to create a function:

  ```javascript
  function functionName(parameter1, parameter2, ...) {
  // Code to be executed
  return result; // Optional: Return a value
  }
  ```

  Here's a breakdown of the syntax:

  - **`function`**: This is the keyword used to declare a function in JavaScript.

  - **`functionName`**: This is the name you choose for your function. It should be a valid identifier (follow variable naming rules).

  - **`parameter1`**, **`parameter2`**, **`...`** : These are the input parameters that the function can accept. They are optional, and you can have none or multiple parameters.

  - **`return result`**: This is an optional statement used to return a value from the function. If omitted, the function will return undefined.

- Here's an example of a simple function that adds two numbers:

  ```javascript
  function addNumbers(a, b) {
    var sum = a + b;
    return sum;
  }

  //You can call this function by using its name and passing arguments:
  const result = addNumbers(5, 3); // result will be 8
  ```

- Remember, you can also create anonymous functions (functions without a name) and assign them to variables, or use them as arguments to other functions. This is often used in scenarios like callbacks or when creating functions on the fly.
