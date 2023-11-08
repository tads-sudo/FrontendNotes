# How to return from a function?

- In JavaScript, you can use the return statement to exit a function and optionally return a value to the caller.

  Here's an example:

  ```javascript
  function add(x, y) {
    return x + y; // This returns the sum of x and y
  }

  let result = add(3, 5); // The function is called with arguments 3 and 5, and the result is returned and stored in the variable 'result'
  console.log(result); // This will print 8
  ```

  In the example above, the add function takes two parameters x and y, adds them together, and then uses the return statement to return the result back to the caller.

- If a function doesn't have a return statement, it implicitly returns undefined.

  Here's an example of a function without a return statement:

  ```javascript
  function sayHello() {
    console.log("Hello!");
  }

  let greeting = sayHello(); // This will print "Hello!" but 'greeting' will be undefined
  console.log(greeting); // This will print 'undefined'
  ```

  In this case, sayHello prints "Hello!" to the console, but it doesn't return anything, so the variable greeting will be undefined.
