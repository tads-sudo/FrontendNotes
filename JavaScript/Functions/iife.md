# Immediately Invoked Function Expression (IIFE)

- It is a design pattern used in JavaScript to create a function and immediately execute it.

- Here's an example of an IIFE:

  ```javascript
  (function () {
    // code here
  })();
  ```

  In this example, an anonymous function is defined and wrapped in parentheses. The trailing () immediately invokes the function.

- IIFE helps in creating a private scope for variables and functions, preventing them from polluting the global namespace. This means they are not accessible outside of the IIFE, which helps prevent naming conflicts and collisions with variables and functions from other parts of your code or from third-party libraries.

  For example, consider the following code:

  ```javascript
  (function () {
    var privateVariable = "This is private";

    function privateFunction() {
      console.log("This is a private function");
    }

    // These variables and functions are not accessible outside of the IIFE
  })();
  ```

  In this example, privateVariable and privateFunction are scoped to the IIFE and cannot be accessed from outside of it. This helps keep your code modular and organized, and reduces the risk of unintended interactions with other parts of your codebase or external libraries.

- IIFE can also take arguments:

  ```javascript
  (function (name) {
    console.log("Hello, " + name);
  })("John");
  ```

  In this example, the function takes an argument name and immediately logs a message to the console.

- IIFE is often used to encapsulate code and avoid naming conflicts, especially when working with libraries or multiple scripts on a page. It's also commonly used in module patterns to create private variables and functions.

- **`KEEP IN MIND`** that with modern JavaScript and the introduction of modules (ES6 Modules), the need for IIFEs has decreased somewhat, as modules provide a more structured and organized way to encapsulate code.
