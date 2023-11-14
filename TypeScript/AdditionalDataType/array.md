# Array

- You can define an array type using the syntax `Type[]` or `Array<Type>`, where Type is the type of elements that the array can contain.

- Here are a few examples:

  ```typescript
  // Array of numbers
  let numbers: number[] = [1, 2, 3, 4, 5];

  // Same as above using Array<Type> syntax
  let numbersArray: Array<number> = [1, 2, 3, 4, 5];

  // Array of strings
  let strings: string[] = ["apple", "banana", "cherry"];

  // Array of booleans
  let booleans: boolean[] = [true, false, true];

  // Array of objects
  interface Person {
    name: string;
    age: number;
  }

  let people: Person[] = [
    { name: "Alice", age: 25 },
    { name: "Bob", age: 30 },
    { name: "Charlie", age: 22 },
  ];
  ```

- You can also use the Array type with a tuple to specify the types and lengths of individual elements in the array:

  ```typescript
  // Tuple array: Each element is a tuple with a string and a number
  let tupleArray: [string, number][] = [
    ["apple", 5],
    ["banana", 3],
    ["cherry", 8],
  ];
  ```

- Additionally, TypeScript supports generics, so you can create reusable array types with a specific element type:

  ```typescript
  // Generic array type
  function createArray<T>(length: number, value: T): T[] {
    return Array.from({ length }, () => value);
  }

  let numberArray: number[] = createArray(5, 0); // [0, 0, 0, 0, 0]
  let stringArray: string[] = createArray(3, "hello"); // ["hello", "hello", "hello"]
  ```
