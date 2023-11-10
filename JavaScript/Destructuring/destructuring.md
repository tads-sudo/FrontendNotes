# Destructuring

- Is a feature in JavaScript that allows you to extract values from arrays or properties from objects and bind them to variables in a more concise and convenient way.

- **`Destructuring Arrays`**:

  1. **`Basic Array Destructuring`**:

     ```javascript
     const numbers = [1, 2, 3, 4, 5];

     // Destructuring assignment
     const [first, second, , fourth] = numbers;

     console.log(first); // 1
     console.log(second); // 2
     console.log(fourth); // 4
     ```

  2. **`Swapping Variables`**:

     ```javascript
     let a = 1;
     let b = 2;

     // Swapping with array destructuring
     [a, b] = [b, a];

     console.log(a); // 2
     console.log(b); // 1
     ```

- **`Destructuring Objects`**:

  1. **`Basic Object Destructuring`**:

     ```javascript
     const person = { name: "John", age: 30, city: "New York" };

     // Destructuring assignment
     const { name, age, city } = person;

     console.log(name); // John
     console.log(age); // 30
     console.log(city); // New York
     ```

  2. **`Renaming Variables`**:

     ```javascript
     const person = { name: "John", age: 30, city: "New York" };

     // Destructuring assignment with variable renaming
     const { name: fullName, age: years, city: residence } = person;

     console.log(fullName); // John
     console.log(years); // 30
     console.log(residence); // New York
     ```

- **`Destructuring Function Parameters`**:

  ```javascript
  // Using object destructuring in function parameters
  function printPerson({ name, age }) {
    console.log(`${name} is ${age} years old.`);
  }

  const person = { name: "Alice", age: 25 };
  printPerson(person);
  // Output: Alice is 25 years old.
  ```

- **`Nested Destructuring`**:

  ```javascript
  const user = {
    id: 1,
    username: "john_doe",
    details: {
      firstName: "John",
      lastName: "Doe",
      address: {
        city: "New York",
        country: "USA",
      },
    },
  };

  // Nested object destructuring
  const {
    username,
    details: {
      firstName,
      address: { city },
    },
  } = user;

  console.log(username); // john_doe
  console.log(firstName); // John
  console.log(city); // New York
  ```
