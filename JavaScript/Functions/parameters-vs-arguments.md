# Parameters and Arguments

- They have different meanings in the context of functions.

  1.  **`Parameters`**:

      - Parameters are the names listed in the function definition.

      - They act as placeholders for the values that the function will receive when it is called.

      - They are defined as part of the function signature.

      - Parameters are used to specify what kind of values the function expects to receive.

        Example:

        ```javascript
        function addNumbers(a, b) {
          // 'a' and 'b' are parameters
          return a + b;
        }
        ```

        In this example, a and b are the parameters of the addNumbers function.

  2.  **`Arguments`**:

      - Arguments are the actual values that are passed to a function when it is called.

      - They are provided within the parentheses when you call a function.

      - The number of arguments must match the number of parameters the function expects.

        Example:

        ```javascript
        let result = addNumbers(5, 3);

        // Here, '5' and '3' are arguments passed to the function.
        ```

        In this case, 5 and 3 are the arguments that are passed to the addNumbers function when it is called.

- **`IN SUMMARY`**, parameters are the placeholders defined in the function declaration, while arguments are the actual values passed to the function when it is called. The number of arguments must match the number of parameters specified in the function declaration.
