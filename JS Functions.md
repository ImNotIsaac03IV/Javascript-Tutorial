# Functions in JavaScript - Review

## Key Concepts
1. **What is a Function?**
   - A reusable block of code that groups together statements to perform a specific task.

2. **Function Declaration**:
   - Syntax:
     ```javascript
     function functionName(parameter1, parameter2) {
       // Code to execute
     }
     ```
   - Example:
     ```javascript
     function greet(name) {
       console.log(`Hello, ${name}!`);
     }
     ```

3. **Parameters and Arguments**:
   - **Parameter**: A named variable inside a function’s block.
   - **Argument**: The value passed to the function when it is invoked.
   - Example:
     ```javascript
     function add(a, b) {
       return a + b;
     }
     add(3, 5); // 8
     ```

4. **Invoking a Function**:
   - Call a function by using its name followed by parentheses.
   - Example:
     ```javascript
     greet('Alice'); // "Hello, Alice!"
     ```

5. **Default Parameters (ES6)**:
   - Assign a default value to a parameter if no argument is passed.
   - Example:
     ```javascript
     function greet(name = 'Guest') {
       console.log(`Hello, ${name}!`);
     }
     greet(); // "Hello, Guest!"
     ```

6. **Return Statement**:
   - Used to return a value from a function.
   - Example:
     ```javascript
     function multiply(a, b) {
       return a * b;
     }
     const result = multiply(2, 3); // 6
     ```

7. **Function Expressions**:
   - A function assigned to a variable.
   - Example:
     ```javascript
     const greet = function(name) {
       console.log(`Hello, ${name}!`);
     };
     greet('Bob'); // "Hello, Bob!"
     ```

8. **Arrow Functions (ES6)**:
   - A concise way to write functions.
   - Syntax:
     ```javascript
     const functionName = (parameter1, parameter2) => {
       // Code to execute
     };
     ```
   - Example:
     ```javascript
     const greet = (name) => {
       console.log(`Hello, ${name}!`);
     };
     greet('Charlie'); // "Hello, Charlie!"
     ```

9. **Concise Arrow Notation**:
   - For single-line functions, omit `{}` and `return`.
   - Example:
     ```javascript
     const add = (a, b) => a + b;
     console.log(add(2, 3)); // 5
     ```

---

## Differences Between Function Types
- **Function Declarations**:
  - Hoisted (can be called before declaration).
  - Syntax: `function name() {}`.
- **Function Expressions**:
  - Not hoisted.
  - Syntax: `const name = function() {}`.
- **Arrow Functions**:
  - Not hoisted.
  - No `this` binding (inherits `this` from the parent scope).
  - Syntax: `const name = () => {}`.

---

## Example Code
```javascript
// Function Declaration
function greet(name) {
  console.log(`Hello, ${name}!`);
}
greet('Alice'); // "Hello, Alice!"

// Function Expression
const greetExpression = function(name) {
  console.log(`Hello, ${name}!`);
};
greetExpression('Bob'); // "Hello, Bob!"

// Arrow Function
const greetArrow = (name) => {
  console.log(`Hello, ${name}!`);
};
greetArrow('Charlie'); // "Hello, Charlie!"

// Concise Arrow Function
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5

// Default Parameters
function greetDefault(name = 'Guest') {
  console.log(`Hello, ${name}!`);
}
greetDefault(); // "Hello, Guest!"