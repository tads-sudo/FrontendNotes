# Callback Function

- A callback function is a function that is passed as an argument to another function and is executed after the completion of that function. This allows you to perform actions asynchronously or in response to events.

- Here's an example to illustrate how callback functions work:

  ```javascript
  function doSomething(callback) {
    // Perform some task
    // ...

    // Call the callback function
    callback();
  }

  function callbackFunction() {
    console.log("Callback function executed");
  }

  // Pass the callback function as an argument

  doSomething(callbackFunction);
  ```

  In this example, _**doSomething**_ is a function that takes another function (_**callback**_) as an argument. Inside _**doSomething**_, it performs some task and then calls the _**callback**_ function.

  The callbackFunction is defined separately and it simply logs a message to the console.

  When _**doSomething**_ is called with _**callbackFunction**_ as an argument, it will execute the task and then call _**callbackFunction**_, resulting in the message "Callback function executed" being printed to the console.

- Callback functions are commonly used in asynchronous programming, where you want to perform tasks that may take some time (like fetching data from a server), and you want to specify what to do after the task is completed.

- For example, in Node.js, you often use callback functions with functions that perform I/O operations (like reading a file or making an HTTP request) because these operations are non-blocking and asynchronous by nature.

- **`KEEP IN MIND`** that with the advent of ES6 and later versions of JavaScript, there are other mechanisms like Promises and async/await that provide cleaner and more structured ways to handle asynchronous code compared to just using callbacks.
