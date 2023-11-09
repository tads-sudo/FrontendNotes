# Function Scope

- Function scope refers to the visibility or accessibility of variables and functions within a particular function.

- Variables and functions defined within a function are typically only accessible within that function and any nested functions.

- Here's an example to illustrate function scope:

  ```javascript
  function outerFunction() {
    var outerVariable = "I'm a variable in outerFunction";

    function innerFunction() {
      var innerVariable = "I'm a variable in innerFunction";
      console.log(outerVariable); // Accessible because innerFunction can access outerFunction's scope
      console.log(innerVariable); // Accessible within innerFunction
    }

    console.log(outerVariable); // Accessible within outerFunction
    console.log(innerVariable); // Not accessible, as it's defined in innerFunction's scope

    innerFunction();
  }

  outerFunction();
  ```

  In this example, outerVariable is defined in the scope of outerFunction, so it is accessible within outerFunction and any functions defined within it, such as innerFunction. innerVariable is only accessible within innerFunction.

- Variables defined outside of any function, i.e., in the global scope, are accessible throughout the entire script. For example:

  ```javascript
  var globalVariable = "I'm a global variable";

  function myFunction() {
    console.log(globalVariable); // Accessible within myFunction because it's in the global scope
  }

  myFunction();
  console.log(globalVariable); // Accessible globally
  ```
