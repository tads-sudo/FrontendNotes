# Enums

- enums (short for enumerations) allow you to define a set of named numeric values.

- Enums are useful when you have a fixed set of related constants. Here's a basic example of how enums work in TypeScript:

  ```typescript
  // Numeric Enum
  enum Direction {
    Up,
    Down,
    Left,
    Right,
  }

  let myDirection: Direction = Direction.Up;
  console.log(myDirection); // Output: 0

  // String Enum
  enum Color {
    Red = "RED",
    Green = "GREEN",
    Blue = "BLUE",
  }

  let myColor: Color = Color.Green;
  console.log(myColor); // Output: "GREEN"
  ```

  In the example above:

  1. The `Direction` enum assigns numeric values starting from 0 by default. You can also explicitly set the values if needed, like `enum Direction { Up = 1, Down = 2, Left = 3, Right = 4 }` or enum Direction { Up = 1, Down, Left, Right }.
  2. The `Color` enum assigns string values to each member.

- Enums in TypeScript can be used in various ways. For example:

  - **`Accessing Enum Values`**:

    ```typescript
    console.log(Direction.Up); // Output: 0
    console.log(Color.Red); // Output: "RED"
    ```

  - **`Enum Type Safety`**:

    ```typescript
    // This will result in a TypeScript error since 5 is not a valid value of the Direction enum.
    // The line below will result in a compilation error.
    let invalidDirection: Direction = 5;
    ```

  - **`Reverse Mapping`**: Enums in TypeScript also support reverse mapping, which means you can get the name of an enum member from its value:

    ```typescript
    let directionValue: number = 2;
    let directionName: string = Direction[directionValue];
    console.log(directionName); // Output: "Left"
    ```

  - **`Using Enums in Functions`**:

    ```typescript
    function move(direction: Direction): void {
      // ...
    }

    move(Direction.Right);
    ```
