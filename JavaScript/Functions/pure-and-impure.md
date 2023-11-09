# Pure Function and Impure Function

- Functions can be categorized into two main types: pure functions and impure functions.

  1. **`Pure Functions`**:

     - A pure function is a function that, given the same input, will always return the same output and has no side effects.
     - It doesn't modify any variables or states outside its scope.
     - It relies only on its input parameters to compute the result.
     - It doesn't interact with external resources, such as databases or APIs.
     - Pure functions are deterministic, which means that for a given set of inputs, they will always produce the same output.
     - Example of a pure function:

       ```javascript
       function add(a, b) {
         return a + b;
       }
       ```

  2. **`Impure Functions`**:

     - An impure function is a function that can have side effects or produce different output for the same input.
     - It may modify variables or states outside its scope.
     - It may rely on external resources or have interactions with the environment.
     - Example of an impure function:

       ```javascript
       let total = 10;

       function addToTotal(value = 0) {
         total += value;
         return total;
       }

       console.log(addToTotal());
       ```

       In this example, the addToTotal function modifies the total variable outside its scope, which makes it impure.

- Impure functions are not necessarily bad, and they are often necessary in practical programming, especially when you need to interact with the external world or manage state. However, understanding the difference between pure and impure functions can help you write more maintainable and predictable code.

- Using pure functions wherever possible can lead to benefits like easier testing, improved code maintainability, and better reasoning about your code's behavior. However, it's important to strike a balance between using pure functions and impure functions based on the specific requirements of your application.
