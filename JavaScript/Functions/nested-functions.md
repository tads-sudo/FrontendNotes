# Nested Functions

- You can define functions inside other functions. These are known as nested functions or inner functions. Here's an example to demonstrate how nested functions work:

  ```javascript
  function outerFunction() {
    // This is the outer function

    function innerFunction() {
      // This is the inner function
      console.log("Inner function is called");
    }

    innerFunction(); // Calling the inner function
  }

  outerFunction(); // Calling the outer function
  ```

  In this example, outerFunction contains an inner function called innerFunction. When outerFunction is called, it also calls innerFunction.

- **`KEEP IN MIND`** that the inner function has access to variables in the outer function's scope, which is known as `lexical scoping` or `closure`. Here's an example to illustrate this:

  ```javascript
  function outerFunction() {
    let outerVariable = "Hello";

    function innerFunction() {
      console.log(outerVariable); // Accessing outerVariable from the outer function's scope
    }

    innerFunction();
  }

  outerFunction(); // Output: Hello
  ```

- **`HOWEVER`**, the outer function cannot directly access variables defined inside the inner function.

  ```javascript
  function outerFunction() {
    function innerFunction() {
      let innerVariable = "World";
    }

    innerFunction();

    // This will cause an error because innerVariable is not defined in the outer function's scope.
    console.log(innerVariable);
  }

  outerFunction(); // This will result in an error
  ```

- It's important to note that the inner function can also return values or be passed as a reference to other parts of your code, just like any other function.

  ```javascript
  function outerFunction() {
    function innerFunction() {
      return "Inner function value";
    }

    return innerFunction;
  }

  const inner = outerFunction();
  console.log(inner()); // Output: Inner function value
  ```

  This example shows that outerFunction returns innerFunction, and when we call inner, it executes innerFunction and returns its value.
