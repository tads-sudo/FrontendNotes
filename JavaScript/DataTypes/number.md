# Number

- is used to represent both integer and floating-point numbers. It is a primitive data type, which means it is immutable and operates by value.

  Here are some characteristics of the JavaScript "number" data type:

  1.  **Integer and Floating-Point Numbers**: JavaScript does not differentiate between integers and floating-point numbers. All numbers in JavaScript, whether they have a decimal point or not, are of the "number" type.

      ```javascript
      let integerNumber = 42;
      let floatNumber = 3.14;

      console.log(typeof integerNumber);
      console.log(typeof floatNumber);
      ```

  2.  **Floating-Point Precision**: JavaScript uses the IEEE 754 standard to represent numbers, which can sometimes lead to precision issues with floating-point arithmetic.

      ```javascript
      console.log(0.1 + 0.2); // Outputs: 0.30000000000000004
      ```

  3.  **Infinity and -Infinity**: JavaScript has special values for positive infinity (Infinity) and negative infinity (-Infinity).

      ```javascript
      let positiveInfinity = Infinity;
      let negativeInfinity = -Infinity;

      console.log(positiveInfinity);
      console.log(negativeInfinity);
      ```

  4.  **NaN (Not a Number)**: This is a special value representing an unrepresentable value. For example, dividing zero by zero results in NaN.

      ```javascript
      let result = 0 / 0; // NaN

      console.log(result);
      ```

  5.  **Arithmetic Operations**: You can perform various arithmetic operations on numbers in JavaScript using operators like (+, -, \*, /, and %) (modulo).

      ```javascript
      let sum = 10 + 5; // 15
      let difference = 10 - 5; // 5
      let product = 10 * 5; // 50
      let quotient = 10 / 5; // 2
      let remainder = 10 % 3; // 1

      console.log(sum, difference, product, quotient, remainder);
      ```

  6.  **Math Object**: JavaScript provides a built-in Math object that contains many useful functions for mathematical operations.

      ```javascript
      let squareRoot = Math.sqrt(16); // 4
      let randomNum = Math.random(); // Generates a random number between 0 and 1

      console.log(squareRoot);
      console.log(randomNum);
      ```

  7.  **Type Coercion**: JavaScript may perform implicit type coercion when using operators with different types.

      For example:

      ```javascript
      let num = 10;
      let str = "5";

      let result = num + str;
      console.log(result); //105
      ```

      In this example, num is a number (integer) and str is a string. The + operator is used for addition, but since one of the operands is a string, JavaScript will perform an implicit type coercion. It will convert the num value to a string and concatenate the two strings, resulting in the string "105".

  8.  **Limits**: JavaScript numbers are 64-bit floating-point values, which means they can represent values from approximately 5e-324 to 1.8e308.
