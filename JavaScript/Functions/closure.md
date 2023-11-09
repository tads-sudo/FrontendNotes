# Closure

- In JavaScript, "closure" refers to the ability of a function to remember and access its lexical scope even after it's been executed and has returned. This means that a function can access variables and parameters from its outer function, even after the outer function has finished executing.

  Here's an example to illustrate how closures work:

  ```javascript
  function outerFunction() {
    let outerVariable = "I am from the outer function";

    function innerFunction() {
      console.log(outerVariable);
    }

    return innerFunction;
  }

  const closure = outerFunction();
  closure(); // Output: "I am from the outer function"
  ```

  In this example, **_outerFunction_** defines a variable **_outerVariable_** and a nested function **_innerFunction_**. **_innerFunction_** can access **_outerVariable_** because it's in the lexical scope of **_outerFunction_**. When **_outerFunction_** is called, it returns **_innerFunction_**, creating a closure. When closure is subsequently called, it still has access to **_outerVariable_** even though **_outerFunction_** has finished executing.

- Closures are powerful in JavaScript and are commonly used for creating private variables and functions, and for implementing various design patterns.

- **`CAUTION`**: It's worth noting that closures can lead to memory leaks if not used carefully. If a closure maintains references to objects or variables that are no longer needed, those objects will not be garbage collected by the JavaScript engine. To mitigate this, you can be mindful of what variables are captured in the closure and consider techniques like explicitly nullifying references when they are no longer needed.
