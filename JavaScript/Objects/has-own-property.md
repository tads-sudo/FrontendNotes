# hasOwnProperty

- Is a method in JavaScript that is used to check whether an object has a property with a specified name. It returns a boolean value indicating whether the object has the property or not.

  Here's how you can use hasOwnProperty:

  ```javascript
  const myObject = {
    prop1: "value1",
    prop2: "value2",
  };

  console.log(myObject.hasOwnProperty("prop1")); // true
  console.log(myObject.hasOwnProperty("prop3")); // false
  ```
