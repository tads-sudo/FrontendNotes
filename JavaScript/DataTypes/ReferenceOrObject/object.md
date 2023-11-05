# Object

- In JavaScript, objects are a fundamental data type that allow you to group related data and functionality together.

- They are a collection of key-value pairs where `the keys are strings (or Symbols, in more advanced use cases)` and `the values can be any data type, including other objects`

  Including other objects?

  Yes! In JavaScript, you can have objects as values within other objects. This allows you to create complex data structures where objects can contain other objects as properties.

  For example:

  ```javascript
  let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    address: {
      street: "123 Main St",
      city: "New York",
      state: "NY",
    },
  };

  //In this example, the person object has a property called address, which is another object containing information about the person's address. The address object has its own properties (street, city, and state).
  ```

- You can access properties of nested objects using multiple levels of dot notation or square bracket notation:

  ```javascript
  console.log(person.address.street); // Output: "123 Main St"

  console.log(person["address"]["city"]); // Output: "New York"
  ```

- Objects in JavaScript are mutable, which means their properties can be changed after they are created. You can also add or remove properties dynamically.

  ```javascript
  let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    address: {
      street: "123 Main St",
      city: "New York",
      state: "NY",
    },
  };

  person.age = 31; // Modify the age property

  person.middleName = "middle"; // Add a new property

  delete person.lastName; // Remove the lastName property
  ```

- There are several ways to create objects in JavaScript:

  1. **Object Literal Notation**:

     ```javascript
     let person = {
       firstName: "John",
       lastName: "Doe",
       age: 30,
     };
     ```

  2. **Using the new keyword with Object constructor**:

     ```javascript
     let person = new Object();
     person.firstName = "John";
     person.lastName = "Doe";
     person.age = 30;
     ```

  3. **Using a Constructor Function**:

     ```javascript
     function Person(firstName, lastName, age) {
       this.firstName = firstName;
       this.lastName = lastName;
       this.age = age;
     }

     let person = new Person("John", "Doe", 30);
     ```

  4. **Using ES6 Classes**:

     ```javascript
     class Person {
       constructor(firstName, lastName, age) {
         this.firstName = firstName;
         this.lastName = lastName;
         this.age = age;
       }
     }

     let person = new Person("John", "Doe", 30);
     ```

  5. **Using Object.create()**:

     ```javascript
     let personPrototype = {
       firstName: "",
       lastName: "",
       age: 0,
     };

     let person = Object.create(personPrototype);
     person.firstName = "John";
     person.lastName = "Doe";
     person.age = 30;
     ```
