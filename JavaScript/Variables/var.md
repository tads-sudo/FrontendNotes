# Var

- Is a keyword used to declare variables. It was traditionally used to declare variables before the introduction of let and const in ECMAScript 6 (ES6).

- Here's an example of how you can use var to declare a variable:

  ```javascript
  var message = "Hello, world!";
  ```

  In this example, a variable named message is declared and initialized with the string "Hello, world!".

- It's important to note that variables declared with var have function scope, which means they are accessible within the function they are declared in, and they can also be accessed outside of blocks, which can sometimes lead to unexpected behavior.

  For example:

  ```javascript
  function example() {
    var localVar = "I'm a local variable";
    if (true) {
      var anotherVar = "I'm accessible outside the if block";
    }
    console.log(localVar); // This will work
    console.log(anotherVar); // This will also work
  }
  console.log(localVar); // This will result in an error
  console.log(anotherVar); // This will also result in an error
  example();
  ```

- In modern JavaScript, it's recommended to use let and const for variable declarations as they have block scope, which helps prevent certain types of bugs that can occur with var.

  For example:

  ```javascript
  function example() {
    let localVar = "I'm a local variable";
    if (true) {
      let anotherVar = "I'm only accessible within the if block";
      console.log(anotherVar); // This will work
    }
    console.log(localVar); // This will work
    console.log(anotherVar); // This will result in an error
  }
  example();
  ```

- If a var variable is declared outside of any function or block, it becomes a global variable. This means it can be accessed and modified from anywhere in your JavaScript code, including other functions, blocks, or scripts.

  Here's an example:

  ```javascript
  var globalVariable = "I'm a global variable";

  function myFunction() {
    console.log(globalVariable); // This will print: "I'm a global variable"
  }

  console.log(globalVariable); // This will print: "Modified global variable"

  globalVariable = "Modified global variable"; // Modifying the global variable

  console.log(globalVariable); // This will print: "Modified global variable"

  myFunction();
  ```
