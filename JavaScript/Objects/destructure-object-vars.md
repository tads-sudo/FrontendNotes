# Destructuring object as variable

- Destructuring in JavaScript allows you to extract values from objects or arrays and assign them to variables. When destructuring objects, you can use curly braces {} to specify the properties you want to extract. Here's an example of destructuring an object into variables:

  ```javascript
  const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
  };

  const { firstName, lastName, age } = person;

  console.log(firstName); // Output: John
  console.log(lastName); // Output: Doe
  console.log(age); // Output: 30
  ```

- You can also destructure nested objects:

  ```javascript
  const person = {
    name: {
      firstName: "John",
      lastName: "Doe",
    },
    age: 30,
  };

  const {
    name: { firstName, lastName },
    age,
  } = person;

  console.log(firstName); // Output: John
  console.log(lastName); // Output: Doe
  console.log(age); // Output: 30
  ```

- If the variable names you want to use differ from the property names, you can specify new variable names using a syntax like this:

  ```javascript
  const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
  };

  const { firstName: first, lastName: last, age: personAge } = person;

  console.log(first); // Output: John
  console.log(last); // Output: Doe
  console.log(personAge); // Output: 30
  ```
