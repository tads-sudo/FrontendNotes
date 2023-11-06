# Creating object method

- you can create methods for objects by adding functions as properties of the object.

  Here's an example of how you can do this:

  ```javascript
  // Define an object
  let person = {
    firstName: "John",
    lastName: "Doe",
    fullName: function () {
      return this.firstName + " " + this.lastName;
    },
  };

  // Access the method
  console.log(person.fullName()); // Output: John Doe
  ```

  In this example, person is an object with properties firstName, lastName, and a method fullName. The fullName method is a function that concatenates the firstName and lastName properties of the object.

  You can also define object methods using ES6 class syntax:

  ```javascript
  class Person {
    constructor(firstName, lastName) {
      this.firstName = firstName;
      this.lastName = lastName;
    }

    fullName() {
      return this.firstName + " " + this.lastName;
    }
  }

  let person = new Person("John", "Doe");

  console.log(person.fullName()); // Output: John Doe
  ```

  In this example, we define a class Person with a constructor method to set the firstName and lastName properties. We also have a fullName method that concatenates these properties.

  Both approaches achieve the same result, but the second example uses ES6 class syntax, which provides a more structured way of creating objects with methods.
