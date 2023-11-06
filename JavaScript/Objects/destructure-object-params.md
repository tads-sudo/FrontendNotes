# Destructuring object as parameters

- You can destructure object parameters using object destructuring. This allows you to extract specific properties from an object and assign them to variables in a more concise and readable way.

  Here's an example of how you can destructure object parameters:

  ```javascript
  const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
  };

  function printPersonDetails({ firstName, lastName, age }) {
    console.log(`First Name: ${firstName}`);
    console.log(`Last Name: ${lastName}`);
    console.log(`Age: ${age}`);
  }

  printPersonDetails(person);
  ```

- You can also provide default values in case the property is not present in the object:

  ```javascript
  const person = {
    firstName: "Jane",
    age: 25,
  };

  function printPersonDetails({
    firstName = "John",
    lastName = "Doe",
    age = 18,
  }) {
    console.log(`First Name: ${firstName}`);
    console.log(`Last Name: ${lastName}`);
    console.log(`Age: ${age}`);
  }

  printPersonDetails(person);
  ```

  In this example, if the lastName property is not present in the person object, it will default to 'Doe'.

- Additionally, you can alias the variable names by using a different name after the colon:

  ```javascript
  const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
  };

  function printPersonDetails({ firstName: first, lastName: last, age }) {
    console.log(`First Name: ${first}`);
    console.log(`Last Name: ${last}`);
    console.log(`Age: ${age}`);
  }

  printPersonDetails(person);
  ```

  In this case, firstName is aliased to first and lastName is aliased to last.

- `REMEMBER` that the property names you use in the destructuring pattern must match the actual property names in the object. If they don't, the variables will be assigned undefined.

- `KEEP IN MIND` that object destructuring is a feature introduced in ECMAScript 6 (ES6), so if you're working in an environment that doesn't support ES6, you may need to use a transpiler like Babel to convert your code to an older version of JavaScript that is supported.
