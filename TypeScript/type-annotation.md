# Type Annotation

- TypeScript is a statically typed superset of JavaScript, and one of its main features is static typing. Type annotations are used to specify the types of variables, parameters, and return values in your code.

- Here's a brief overview of how type annotations are used in TypeScript:

  1.  **Variable Declaration**:

      ```typescript
      let myVariable: number; // Type annotation for a variable
      myVariable = 10;
      ```

  2.  **Function Parameters and Return Types**:

      ```typescript
      function add(a: number, b: number): number {
        // Type annotations for function parameters and return type
        return a + b;
      }
      ```

  3.  **Object Types**:

      ```typescript
      let person: { name: string; age: number }; // Type annotation for an object
      person = { name: "John", age: 30 };
      ```

  4.  **Array Types**:

      ```typescript
      let numbers: number[]; // Type annotation for an array

      numbers = [1, 2, 3, 4];
      ```

  5.  **Union Types**:

      ```typescript
      let result: string | number; // Type annotation for a variable that can hold either a string or a number

      result = "Hello";
      result = 42;
      ```

  6.  Type Aliases:

      ```typescript
      type Point = { x: number; y: number }; // Type alias for an object type

      let coordinates: Point;
      coordinates = { x: 10, y: 20 };
      ```
