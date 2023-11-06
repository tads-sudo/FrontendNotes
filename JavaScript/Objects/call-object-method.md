# Calling object method

- you can call an object's method using dot notation or bracket notation.

  Here's an example using dot notation:

  ```javascript
  const myObject = {
    myMethod: function () {
      console.log("This is my method.");
    },
  };

  myObject.myMethod(); // This will call the method and print "This is my method."
  ```

  And here's an example using bracket notation:

  ```javascript
  const myObject = {
    myMethod: function () {
      console.log("This is my method.");
    },
  };

  myObject["myMethod"](); // This will also call the method and print "This is my method."
  ```

  Both of these examples achieve the same result, which is calling the myMethod function of the myObject object.

- If you're using ES6 (ECMAScript 2015) or later, you can use shorthand method syntax like this:

  ```javascript
  const myObject = {
    myMethod() {
      console.log("This is my method.");
    },
  };

  myObject.myMethod(); // This will call the method and print "This is my method."
  ```
