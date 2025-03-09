# Functions as Data and Higher-Order Functions - Review

## Key Concepts
1. **Abstraction**:
   - Simplifies complex code by breaking it into reusable, understandable, and modular pieces.
   - Example:
     ```javascript
     function calculateArea(radius) {
       return Math.PI * radius * radius;
     }
     console.log(calculateArea(5)); // 78.54
     ```

2. **Functions as Data**:
   - Functions can be treated like any other data type (e.g., assigned to variables, passed as arguments, returned from other functions).
   - Example:
     ```javascript
     const greet = function() {
       console.log('Hello!');
     };
     greet(); // "Hello!"
     ```

3. **First-Class Objects**:
   - JavaScript functions are first-class objects, meaning they can have properties and methods like any other object.
   - Example:
     ```javascript
     function sayHello() {
       console.log('Hello!');
     }
     sayHello.description = 'This is a greeting function';
     console.log(sayHello.description); // "This is a greeting function"
     ```

4. **Functions as Parameters**:
   - Functions can be passed into other functions as arguments.
   - Example:
     ```javascript
     function executeFunction(func) {
       func();
     }
     executeFunction(greet); // "Hello!"
     ```

5. **Higher-Order Functions**:
   - A function that either:
     - Accepts a function as a parameter.
     - Returns a function.
     - Or both.
   - Example:
     ```javascript
     function higherOrderFunction(func) {
       return function() {
         console.log('Before executing function');
         func();
         console.log('After executing function');
       };
     }
     const newFunction = higherOrderFunction(greet);
     newFunction();
     // Output:
     // "Before executing function"
     // "Hello!"
     // "After executing function"
     ```

---

## Example Code
```javascript
// Abstraction
function calculateArea(radius) {
  return Math.PI * radius * radius;
}
console.log(calculateArea(5)); // 78.54

// Functions as Data
const greet = function() {
  console.log('Hello!');
};
greet(); // "Hello!"

// Functions as Parameters
function executeFunction(func) {
  func();
}
executeFunction(greet); // "Hello!"

// Higher-Order Function
function higherOrderFunction(func) {
  return function() {
    console.log('Before executing function');
    func();
    console.log('After executing function');
  };
}
const newFunction = higherOrderFunction(greet);
newFunction();
// Output:
// "Before executing function"
// "Hello!"
// "After executing function"