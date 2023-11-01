# const

- Keyword const was introduced in ES6(ES2015).

- const is intended to create a block scope variable.

- const variable can't be redeclared and reassign to a new value. Try the code below.

  ```javascript
  if (true) {
    const constVariable = "This is true";
    const constVariable = "This is false";
    console.log(constVariable);
  }
  ```

  Your code editor will show this warning message. Like in the image below.

  ![A typescript error message saying, Cannot redeclare block scoped Variable'constVariable'.](/JavaScript/ScreenshotsOnly/const-cannot-be-redeclared.png "A typescript error message saying, Cannot redeclare block-scoped Variable 'constVariable'.")

- But, if the const variable is holding an object or an array, it does not make the object or array itself immutable. This means that you can still modify the properties or elements of the object or array.

  For example:

  ```javascript
  const myObject = { key: "value" };
  myObject.key = "new value"; // This is allowed, as we are modifying a property of the object

  const myArray = [1, 2, 3];
  myArray[0] = 0; // This is allowed, as we are modifying an element of the array
  ```
