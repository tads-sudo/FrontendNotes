# Creating Object

- You can create objects using different methods. Here are a few common ways:

  1. **Object Literal**: The simplest way to create an object is by using an object literal, which is a comma-separated list of name-value pairs inside curly braces {}.

     ```javascript
     let person = {
       firstName: "John",
       lastName: "Doe",
       age: 30,
       fullName: function () {
         return this.firstName + " " + this.lastName;
       },
     };
     ```

     In this example, person is an object with properties like firstName, lastName, age, and a method fullName.

  2. **Using the new keyword with Constructor Functions**: You can create objects using constructor functions, which are functions designed to create and initialize objects.

     ```javascript
     function Person(firstName, lastName, age) {
       this.firstName = firstName;
       this.lastName = lastName;
       this.age = age;
       this.fullName = function () {
         return this.firstName + " " + this.lastName;
       };
     }

     let person = new Person("John", "Doe", 30);
     ```

     Here, Person is a constructor function. When called with new, it creates a new object and sets the properties and methods defined inside the function.

  3. **Using Object.create()**: You can use the Object.create() method to create a new object with an existing object as its prototype.

     ```javascript
     let personPrototype = {
       fullName: function () {
         return this.firstName + " " + this.lastName;
       },
     };

     let person = Object.create(personPrototype);
     person.firstName = "John";
     person.lastName = "Doe";
     person.age = 30;
     ```

     In this example, person is created with personPrototype as its prototype.

  4. **Using ES6 Classes**: ES6 introduced class syntax, which is a more convenient way to define constructor functions and their prototypes.

     ```javascript
     class Person {
       constructor(firstName, lastName, age) {
         this.firstName = firstName;
         this.lastName = lastName;
         this.age = age;
       }

       fullName() {
         return this.firstName + " " + this.lastName;
       }
     }
     let person = new Person("John", "Doe", 30);
     ```

     Here, Person is a class that can be used to create objects.
