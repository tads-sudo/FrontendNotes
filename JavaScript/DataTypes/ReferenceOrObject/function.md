# Function

- Functions are considered "first-class citizens," which means they can be treated like any other value. This means you can assign functions to variables, pass them as arguments to other functions, and return them as values from other functions.

- The data type of a function in JavaScript is function. You can check the type of a function using the `typeof` operator. For example:

  ```javascript
  function myFunction() {
    // Function body
  }

  console.log(typeof myFunction); // Outputs "function"
  ```

- It's worth noting that functions in JavaScript can also have properties and methods, as they are objects. This means you can attach properties and methods to a function, just like you can with any other object.

  For example:

  ```javascript
  function myFunction() {
    // Function body
  }

  myFunction.myProperty = "Hello";
  console.log(myFunction.myProperty); // Outputs "Hello"
  ```

  However, even though you can attach properties to functions, they are still considered to be of type function in JavaScript.
