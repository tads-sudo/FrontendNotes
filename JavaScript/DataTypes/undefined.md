# Undefined

- Is a primitive data type that represents the absence of a value or the uninitialized state of a variable.

  Here are some key points about the 'undefined' data type in JavaScript:

  1.  **Uninitialized Variables**: If you declare a variable without assigning a value to it, it will have the value undefined by default.

      ```javascript
      let x;
      console.log(x); // Output: undefined
      ```

  2.  **Return Value of Functions**: If a function does not return a value explicitly, it will return undefined by default.

      ```javascript
      function doSomething() {
        // no return statement
      }
      console.log(doSomething()); // Output: undefined
      ```

  3.  **Property Access**: If you try to access a property that does not exist in an object, you will get undefined.

      ```javascript
      let myObject = { key: "value" };
      console.log(myObject.nonExistentKey); // Output: undefined
      ```

  4.  **Falsy Value**: undefined is considered a falsy value in JavaScript, which means it evaluates to false in a Boolean context.

      ```javascript
      if (undefined) {
        console.log("This will not be executed");
      } else {
        console.log("This will be executed");
      }
      ```

  5.  **Type of undefined**: The typeof operator returns the string 'undefined' when applied to an undefined value.

      ```javascript
      let z;
      console.log(typeof z); // Output: "undefined"
      ```
