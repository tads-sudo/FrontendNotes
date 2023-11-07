# Object Inheritance

- Object inheritance is a fundamental concept that allows you to create a new object that inherits properties and methods from an existing object. This is typically achieved through either prototype-based inheritance or class-based inheritance (introduced in ECMAScript 6, also known as ES6).

  1.  **`Prototype-Based Inheritance`**: In JavaScript, each object has a prototype. When you access a property or method on an object, JavaScript will first look for it on the object itself, and if it's not found, it will look in the object's prototype chain. You can create an object that inherits from another object using the Object.create() method or by directly modifying the prototype of a constructor function.

      Here's an example of prototype-based inheritance:

      ```javascript
      // Parent object

      var parent = {
        name: "John",
        greet: function () {
          console.log("Hello, my name is " + this.name);
        },
      };

      // Child object inheriting from the parent
      var child = Object.create(parent);
      child.name = "Alice";

      child.greet(); // This will call the greet method from the parent object with the child's context
      ```

  2.  `Class-Based Inheritance (ES6)`: With the introduction of ES6, JavaScript supports a more class-oriented approach to object-oriented programming. You can define classes using the class keyword and use the extends keyword to inherit from another class. Classes provide a more structured way of working with object inheritance.

      Here's an example of class-based inheritance in ES6:

      ```javascript
      // Parent class
      class Person {
        constructor(name) {
          this.name = name;
        }

        greet() {
          console.log("Hello, my name is " + this.name);
        }
      }

      // Child class inheriting from the Person class
      class Student extends Person {
        constructor(name, studentId) {
          super(name); // Call the constructor of the parent class
          this.studentId = studentId;
        }
      }

      const student = new Student("Alice", 12345);
      student.greet(); // This will call the greet method from the Person class
      ```

  In both cases, you can create a new object that inherits properties and methods from an existing object or class, and you can override or extend those inherited properties and methods as needed. This allows you to implement inheritance in JavaScript for building complex object-oriented structures.
