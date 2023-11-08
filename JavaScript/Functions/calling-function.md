# Function Calls: Parenthesis vs None

- When you call a function without parentheses, you are referring to the function itself rather than executing it.

  For example, if you have a function named myFunction:

  ```javascript
  function myFunction() {
    console.log("Hello!");
  }
  ```

  Calling myFunction without parentheses like this:

  ```javascript
  myFunction;
  ```

  will not execute the function. It simply refers to the function object.

  On the other hand, if you include parentheses:

  ```javascript
  myFunction();
  ```

  this will actually execute the function and perform whatever actions are defined inside it.

- So, to summarize:

  - `myFunction` refers to the function itself.
  - `myFunction()` calls and executes the function.

    It's important to use the appropriate syntax depending on whether you want to refer to the function or actually execute it.
