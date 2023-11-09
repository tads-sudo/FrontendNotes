# Higher Order Function

- Is a function that can take other functions as arguments or return functions as results. This means that you can use functions as values, just like you would with strings or numbers. Higher-order functions enable you to abstract over actions, not just values.

- Here's an example of a higher-order function that takes a function as an argument:

  ```javascript
  function greet(name, greetingFunction) {
    return greetingFunction(name);
  }

  function sayHello(name) {
    return "Hello, " + name + "!";
  }

  function sayGoodbye(name) {
    return "Goodbye, " + name + "!";
  }

  let message = greet("John", sayHello);
  console.log(message); // Output: "Hello, John!"

  message = greet("Jane", sayGoodbye);
  console.log(message); // Output: "Goodbye, Jane!"
  ```

  In this example, greet is a higher-order function because it takes a function (greetingFunction) as one of its arguments.

- Here's an example of a higher-order function that returns a function:

  ```javascript
  function createMultiplier(factor) {
    return function (number) {
      return number * factor;
    };
  }

  let double = createMultiplier(2);
  let triple = createMultiplier(3);

  console.log(double(5)); // Output: 10
  console.log(triple(5)); // Output: 15
  ```

  In this example, createMultiplier is a higher-order function because it returns a new function.
