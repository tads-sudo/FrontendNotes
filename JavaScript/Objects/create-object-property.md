# Creating object property

- you can create object properties in several ways:

  1. **Using Dot Notation**:

     ```javascript
     let myObject = {};
     myObject.propertyName = propertyValue;
     ```

  2. **Using Bracket Notation**:

     ```javascript
     let myObject = {};
     myObject["propertyName"] = propertyValue;
     ```

     This is useful when the property name contains special characters or spaces.

  3. **When Defining an Object Literally**:

     ```javascript
     let myObject = {
       propertyName: propertyValue,
     };
     ```

  4. **Using ES6 Computed Property Names**:

     ```javascript
     let propertyName = "dynamicPropertyName";

     let myObject = {
       [propertyName]: propertyValue,
     };

     console.log(myObject.dynamicPropertyName); // Output: propertyValue
     ```

     In this example, we first define a variable propertyName with the value 'dynamicPropertyName'. When we create the myObject object, we use square brackets [] around propertyName to specify that the property name should be computed based on the value of propertyName.

     As a result, myObject will have a property named dynamicPropertyName with the value 'propertyValue'.

     This feature is particularly useful when you want to dynamically generate property names based on variables or expressions. It allows for more flexibility in creating objects with computed properties.
