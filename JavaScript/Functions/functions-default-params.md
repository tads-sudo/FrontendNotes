# Default Parameters for functions

- You can set default parameters for functions using ES6 (ECMAScript 2015) syntax.

- Default parameters allow you to specify a default value that will be used if an argument is not provided when the function is called.

- Here's an example of a function with default parameters:

  ```javascript
  function greet(name = "Anonymous", greeting = "Hello") {
    console.log(`${greeting}, ${name}!`);
  }

  greet(); // Output: Hello, Anonymous!
  greet("John"); // Output: Hello, John!
  greet("Jane", "Hi"); // Output: Hi, Jane!
  ```

  In this example, the greet function has two parameters (name and greeting). If these parameters are not provided when the function is called, the default values 'Anonymous' and 'Hello' will be used.

- If you want to use a value that evaluates to false (such as 0, null, undefined, etc.) as a default parameter, you can explicitly check for it using a conditional expression:

  ```javascript
  function greet(name = "Anonymous", greeting) {
    greeting = greeting || "Hello"; // If greeting is falsy, use 'Hello'
    console.log(`${greeting}, ${name}!`);
  }

  greet(); // Output: Hello, Anonymous!
  greet("John"); // Output: Hello, John!
  greet("Jane", "Hi"); // Output: Hi, Jane!
  ```

  In this example, if greeting is a falsy value, it will default to 'Hello'.

- **`REMEMBER`** that default parameters are a feature introduced in ECMAScript 2015 (ES6) and may not be supported in older browsers or environments. If you're working in an environment that doesn't support ES6, you may need to use alternative techniques to achieve similar behavior.
