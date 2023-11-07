# Using for...in loop to loop through an object

- for...in loop is used to iterate over the properties of an object. It is typically used with objects that are not arrays, as it is designed for enumerating object properties.

  Here's the basic syntax for a for...in loop:

  ```javascript
  for (variable in object) {
    // code to be executed
  }
  ```

  Here, variable is a variable that will represent the property name, and object is the target object you want to loop through.

  Here's an example of how you might use a for...in loop:

  ```javascript
  const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
  };

  for (let key in person) {
    console.log(`${key}: ${person[key]}`);
  }
  ```

  In this example, the loop iterates over the properties of the person object (firstName, lastName, and age). The key variable will take on the property name in each iteration, allowing you to access the corresponding value using person[key].

- **`KEEP IN MIND`** that for...in also iterates over inherited properties, so it's a good practice to use additional checks (like object.hasOwnProperty(key)) if you want to only loop through the object's own properties.

  Let's say you have an object child that inherits properties from a parent object parent. You want to loop through the properties of child but exclude properties inherited from parent.

  Here's an example:

  ```javascript
  // Parent object
  const parent = {
    inheritedProp: "I am inherited",
    parentOnlyProp: "I am only in parent",
  };

  // Child object inheriting from parent
  const child = Object.create(parent);
  child.childOnlyProp = "I am only in child";

  // Loop through child's properties, but exclude inherited ones
  for (let key in child) {
    if (child.hasOwnProperty(key)) {
      console.log(`${key}: ${child[key]}`);
    }
  }
  ```

  In this example, we have two objects, parent and child. The child object inherits properties from parent through Object.create(parent).

  The for...in loop is used to iterate over the properties of child. However, we use child.hasOwnProperty(key) to check if the property key is directly owned by child and not inherited from its prototype (parent in this case).

  When you run this code, it will only log:

  ```makefile
  childOnlyProp: I am only in child
  ```

  The inheritedProp property from the parent object is excluded from the loop because it is inherited and not directly owned by child.

  This way, you can ensure that you're only working with properties directly defined on the object, not properties inherited from its prototype chain.
