# Let

- Keyword let was introduced in ES6(ES2015).

- Keyword let is intended to create a block scope variable.

  ```javascript
  function start() {
    for (let i = 0; i < 5; i++) {
      console.log(i); //You can only access the variable i here because we know that using "let" keyword to declare "i" variable is only accessible within this block.
    }
    console.log(i); //Let's try to access variable "i" here to prove that using let keyword to declare a variable will make variable not accessible outside the block.
  }

  start();
  ```

- let variable can't be redeclared within the block but you can reassign it to a new value.

  ```javascript
  if (true) {
    let letVariable = "This is true";
    // let letVariable = "This is false";
    letVariable = "This is false";
    console.log(letVariable);
  }
  ```
