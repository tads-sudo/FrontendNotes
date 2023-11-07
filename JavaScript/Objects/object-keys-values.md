# Object.keys and Object.values

- `Object.keys` and `Object.values` are two built-in JavaScript functions that allow you to work with the properties of an object.

  1.  **Object.keys**:

      - The Object.keys function returns an array of a given object's own enumerable property names.

      - It takes an object as an argument and returns an array of strings representing the keys of the object.

      - Example:

      ```javascript
      const person = {
        name: "John",
        age: 30,
        city: "New York",
      };

      const keys = Object.keys(person);

      console.log(keys); // Output: ['name', 'age', 'city']

      //In this example, Object.keys returns an array containing the keys of the person object.
      ```

  2.  **Object.values**:

      - The Object.values function returns an array of a given object's own enumerable property values.

      - It takes an object as an argument and returns an array of values.

      - Example:

        ```javascript
        const person = {
          name: "John",
          age: 30,
          city: "New York",
        };

        const values = Object.values(person);

        console.log(values); // Output: ['John', 30, 'New York']

        //In this example, Object.values returns an array containing the values of the person object.
        ```

  These functions are particularly useful when you want to iterate over the properties of an object or perform operations on the keys or values. Keep in mind that both Object.keys and Object.values only return the enumerable properties of an object, which are properties that can be iterated over in a for...in loop. Non-enumerable properties or properties inherited from the prototype chain will not be included in the result.
