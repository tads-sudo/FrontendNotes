# Accessing object property in JavaScript

- In JavaScript, you can access an object's property using `dot notation` or `bracket notation`.

  Here are the key differences between them:

  1.  **Syntax**:

      - **Dot Notation**: Uses a period (.) followed by the property name.

        ```javascript
        var myObject = {
          property1: "value1",
          property2: "value2",
        };

        console.log(myObject.property1); // Output: 'value1'
        console.log(myObject.property2); // Output: 'value2'
        ```

      - **Bracket Notation**: Uses square brackets [] enclosing the property name as a string.

        ```javascript
        var myObject = {
          property1: "value1",
          property2: "value2",
        };

        console.log(myObject["property1"]); // Output: 'value1'
        console.log(myObject["property2"]); // Output: 'value2'
        ```

  2.  **Property Names**:

      - **Dot Notation**: Requires the property name to be a valid JavaScript identifier (consisting of letters, digits, underscores, and dollar signs). It cannot start with a digit.

      - **Bracket Notation**: Allows property names to be specified as strings, which means they can include special characters, spaces, and even be provided dynamically using variables or expressions.

  3.  **Dynamic Property Access**:

      - In JavaScript, "dynamic property access" refers to the ability to access an object's property using a variable or an expression instead of directly specifying the property name in your code.

        **`Bracket Notation Example`**:

        - Let's consider a more realistic scenario. Imagine you have a function that takes user input or some other form of external input, and you want to use that input to determine which property of an object to access. For example::

          ```javascript
          var myObject = {
            property1: "value1",
            property2: "value2",
          };

          function getProperty(input) {
            return myObject[input];
          }

          var userInput = "property1";
          console.log(getProperty(userInput)); // Output: 'value1'
          ```

          In this example, the getProperty function takes an input parameter. This input could be provided by a user, or come from some other source. The function then uses this input to dynamically access the property of myObject using bracket notation.

          So, the dynamic aspect comes into play when the property you want to access is determined at runtime based on some external condition or input. This allows your code to be more flexible and adaptable to different situations.

        **`Dot Notation Limitation`**:

        - With dot notation, you can't use a variable or an expression to specify the property you want to access. For example, you can't do this:

          ```javascript
          var propertyName = "property1";
          console.log(myObject.propertyName); //This won't works
          ```

          In this case, propertyName is treated as a literal property name, not as a variable holding a property name.

      So, if you need to access object properties dynamically, you must use bracket notation.

      This capability can be particularly useful when you're working with data that may change, or when you want to write more flexible and adaptable code. It allows you to determine which property to access at runtime based on conditions, user input, or other factors.
