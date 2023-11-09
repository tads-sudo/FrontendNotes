# Differences between Callback Function and Higher Order Function

- A callback function and a higher-order function are both concepts in JavaScript that involve the use of functions, but they serve different purposes.

- **`Callback Function`**:

  - A callback function is a function that is passed as an argument to another function.
  - The function receiving the callback function can then execute it at some point during its execution.
  - Callback functions are commonly used in asynchronous programming, where a function doesn't block the execution of the program and instead, it continues to run while it waits for some operation (like fetching data from a server) to complete.
  - Callback functions are used to handle the result of asynchronous operations, making sure that certain code only executes after the asynchronous operation has completed.
  - Example:

    ```javascript
    function doSomethingAsync(callback) {
      setTimeout(function () {
        console.log("Operation completed.");
        callback();
      }, 1000);
    }

    function callbackFunction() {
      console.log("Callback executed.");
    }

    doSomethingAsync(callbackFunction);
    ```

- **`Higher-Order Function`**:

  - A higher-order function is a function that takes one or more functions as arguments, or returns a function as its result.
  - Higher-order functions are used to abstract and generalize the actions or behaviors of other functions.
  - Example:

    ```javascript
    function higherOrderFunction(callback) {
      console.log("Executing higher-order function");
      return function () {
        console.log("Executing callback");
        callback();
      };
    }

    function callbackFunction() {
      console.log("Callback executed.");
    }

    const returnedFunction = higherOrderFunction(callbackFunction);
    returnedFunction();
    ```

    In this example, _higherOrderFunction_ is a higher-order function because it takes _callbackFunction_ as an argument and returns a new function. This returned function, when executed (returnedFunction()), will in turn execute the original _callbackFunction_.
