# Symbol

- In JavaScript, the Symbol data type is a primitive data type introduced in ECMAScript 6 (ES6).

- It is used to create unique and immutable values, which can be used as object property keys.

- Symbols are often used to add non-enumerable properties to objects or to create private members within objects.

- Here's how you create a symbol:

  ```javascript
  const mySymbol = Symbol();
  ```

- You can also provide a description (optional) when creating a symbol, which can be useful for debugging or identifying symbols:

  ```javascript
  const mySymbol = Symbol("my description");
  ```

- Every symbol created using Symbol() is unique, even if they have the same description. For example:

  ```javascript
  const symbol1 = Symbol("my symbol");
  const symbol2 = Symbol("my symbol");

  console.log(symbol1 === symbol2); // false
  ```

- Symbols are primarily used as object property keys. When used as property keys, they are not enumerable in `for...in` loops, and they don't appear in `Object.keys()` or `Object.getOwnPropertyNames()`

  Example with symbols:

  ```javascript
  const mySymbol = Symbol("my symbol");

  const obj = {
    [mySymbol]: "Hello",
  };

  console.log(obj[mySymbol]); // 'Hello'

  for (const key in obj) {
    console.log(key); // Nothing will be logged because the symbol is not enumerable
  }

  console.log(Object.keys(obj)); // []
  ```

  compared to typical object property keys example:

  ```javascript
  const obj = {
    name: "John",
    age: 30,
  };

  for (const key in obj) {
    console.log(key); // 'name', 'age'
  }

  console.log(Object.keys(obj)); // ['name', 'age']
  ```

- Symbols are also used to define well-known symbols that can be used to customize the behavior of objects. For example, the Symbol.iterator symbol is used to define a custom iterator for objects.

  ```javascript
  const myIterable = {
    [Symbol.iterator]: function* () {
      yield 1;
      yield 2;
      yield 3;
    },
  };

  for (const value of myIterable) {
    console.log(value); // 1, 2, 3
  }
  ```

- Overall, symbols provide a way to create unique and non-enumerable properties, which can be useful in certain situations, such as when defining private members or special behaviors for objects.
