# JavaScript Basics Review

## Console Logging
- Use `console.log()` to print data to the console, a panel that displays messages.

## Comments
- Single-line comments: `//`
- Multi-line comments: `/* ... */`

## Data Types
JavaScript has 8 fundamental data types:
1. **Numbers**: Any number without quotes (e.g., `23.8879`).
2. **BigInts**: For very large integers.
3. **Strings**: Characters wrapped in single or double quotes (e.g., `'Sample String'`).
4. **Booleans**: `true` or `false`.
5. **null**: Represents an intentional absence of any object value.
6. **undefined**: Represents a variable that has not been assigned a value.
7. **Symbol**: A unique and immutable primitive value.
8. **Object**: A collection of properties and methods.

## Arithmetic Operators
- Built-in operators: `+`, `-`, `*`, `/`, and `%`.

## Objects
- **Properties**: Stored information accessed with a `.` (e.g., `'Hello'.length`).
- **Methods**: Actions performed by appending the object with a `.`, method name, and parentheses (e.g., `'hello'.toUpperCase()`).

## Built-in Objects
- **Math**: A collection of methods and properties provided by JavaScript.


# Variables in JavaScript - Review

## Key Concepts
- **Variables** hold reusable data in a program and associate it with a name.
- Variables are stored in memory.
- **`var`**: Used in pre-ES6 versions of JavaScript.
- **`let`**: Preferred for variables that can be reassigned.
- **`const`**: Preferred for variables with a constant value.
- Uninitialized variables store the primitive data type `undefined`.
- **Mathematical assignment operators** (e.g., `+=`, `-=`) make it easy to calculate and assign new values to the same variable.
- The **`+` operator** is used to concatenate strings, including string values held in variables.
- **Template literals** (ES6): Use backticks `` ` `` and `${}` to interpolate values into a string.
- **`typeof` keyword**: Returns the data type (as a string) of a value.

---

## Challenges to Explore
1. **Create and Manipulate Variables**:
   - Declare variables using `let`, `const`, and `var`.
   - Reassign values to variables declared with `let`.
   - Try reassigning a value to a variable declared with `const` (observe the error).

2. **Concatenate Strings with Different Data Types**:
   - Combine strings with numbers, booleans, or other data types using the `+` operator.
   - Observe how JavaScript handles the concatenation.

3. **Interpolate Multiple Variables**:
   - Use template literals to interpolate multiple variables into a single string.
   - Example: `` `Hello, my name is ${name} and I am ${age} years old.` ``.

4. **`console.log()` Before Variable Declaration**:
   - Test what happens when you log variables declared with `const`, `let`, and `var` before they are defined.
   - Example:
     ```javascript
     console.log(test1); // What happens?
     const test1 = 'figuring out quirks';
     ```

5. **Use `typeof` to Check Data Types**:
   - Find the data type of a variable’s value using `typeof`.
   - Example: `typeof myVariable`.
   - Use `typeof` to check the data type of the result when concatenating variables of different types (e.g., a string and a number).

---

## Example Code Snippets
```javascript
// Declaring variables
let count = 10;
const name = "Alice";
var isActive = true;

// Mathematical assignment
count += 5; // count is now 15

// String concatenation
let message = "Hello, " + name; // "Hello, Alice"

// Template literals
let info = `Count: ${count}, Active: ${isActive}`; // "Count: 15, Active: true"

// Using typeof
console.log(typeof count); // "number"
console.log(typeof name); // "string"
console.log(typeof (count + name)); // "string"

# JavaScript Versions: ES6 and Before

## What is ES6?
- **ES6** stands for **ECMAScript 6**, the 6th edition of the ECMAScript standard.
- Also referred to as **ES2015** (released in 2015).
- It is the most significant update to JavaScript since its inception in 1997.

---

## A Brief History of JavaScript
- **1995**: JavaScript was introduced by Netscape Communications.
- **1996**: Netscape submitted JavaScript to **Ecma International** to create standards.
- **1997**: Ecma International released **ECMA-262**, the first version of the ECMAScript standard.
- ECMAScript provides the rules and guidelines for JavaScript's architecture.

---

## JavaScript vs. ECMAScript
- **JavaScript**: A scripting language used to create apps and programs.
- **ECMAScript**: A standard for scripting languages. JavaScript follows ECMAScript standards.

---

## Why is ES6 Still Relevant?
- ES6 introduced major features that revolutionized JavaScript development.
- Many modern frameworks (e.g., React) rely on ES6 features.
- ES6 is often referred to as **"Modern JavaScript"** due to its significant improvements.

---

## Key Features of ES6
1. **`let` and `const`**:
   - New ways to declare variables (`let` for reassignable variables, `const` for constants).
2. **Arrow Functions**:
   - Shorter syntax for writing functions.
   - Example:
     ```javascript
     // Pre-ES6
     var greeting = function() {
       console.log('Hello World!');
     };

     // ES6
     const greeting = () => console.log('Hello World!');
     ```
3. **Classes**:
   - Introduced a cleaner syntax for object-oriented programming (OOP).
4. **Default Parameters**:
   - Allows setting default values for function parameters.
5. **Promises**:
   - Improved handling of asynchronous operations.
6. **Template Literals**:
   - Use backticks (`` ` ``) and `${}` for string interpolation.
7. **Many More**:
   - Destructuring, modules, enhanced object literals, etc.

---

## Why Learn ES6?
- **Concise Code**: ES6 allows developers to write cleaner and more efficient code.
- **Modern Frameworks**: Many popular frameworks (e.g., React, Angular, Vue) use ES6 features.
- **Object-Oriented Programming (OOP)**: ES6 makes it easier to use OOP principles in JavaScript.
- **Industry Adoption**: ES6 is widely adopted in the development community.

---

## Legacy Code and Pre-ES6
- Many existing projects still use **pre-ES6 JavaScript**.
- Familiarity with both pre-ES6 and ES6 syntax is essential for working on a wide range of projects.

---

## Example: Pre-ES6 vs. ES6
### Variable Declaration
- **Pre-ES6**:
  ```javascript
  var name = "Alice";

  # Conditionals in JavaScript - Review

## Key Concepts
1. **`if` Statements**:
   - Checks a condition and executes a task if the condition evaluates to `true`.
   - Example:
     ```javascript
     if (condition) {
       // Code to execute if condition is true
     }
     ```

2. **`if...else` Statements**:
   - Makes binary decisions and executes different code blocks based on a condition.
   - Example:
     ```javascript
     if (condition) {
       // Code to execute if condition is true
     } else {
       // Code to execute if condition is false
     }
     ```

3. **`else if` Statements**:
   - Adds more conditions to check if the initial `if` condition is false.
   - Example:
     ```javascript
     if (condition1) {
       // Code to execute if condition1 is true
     } else if (condition2) {
       // Code to execute if condition2 is true
     } else {
       // Code to execute if all conditions are false
     }
     ```

4. **Comparison Operators**:
   - Used to compare two values:
     - `<` (less than)
     - `>` (greater than)
     - `<=` (less than or equal to)
     - `>=` (greater than or equal to)
     - `===` (strict equality)
     - `!==` (strict inequality)
   - Example:
     ```javascript
     if (age >= 18) {
       console.log('You are an adult.');
     }
     ```

5. **Logical Operators**:
   - **`&&` (AND)**: Checks if both expressions are truthy.
     ```javascript
     if (age > 12 && age < 20) {
       console.log('You are a teenager.');
     }
     ```
   - **`||` (OR)**: Checks if either expression is truthy.
     ```javascript
     if (day === 'Saturday' || day === 'Sunday') {
       console.log('It\'s the weekend!');
     }
     ```
   - **`!` (NOT)**: Switches the truthiness of a value.
     ```javascript
     if (!isRaining) {
       console.log('Enjoy the sunshine!');
     }
     ```

6. **Ternary Operator**:
   - Shorthand for simple `if...else` statements.
   - Syntax: `condition ? expressionIfTrue : expressionIfFalse`
   - Example:
     ```javascript
     const message = age >= 18 ? 'You are an adult.' : 'You are a minor.';
     console.log(message);
     ```

7. **`switch` Statements**:
   - Simplifies multiple `else if` statements.
   - Use `break` to stop the remaining cases from being checked.
   - Example:
     ```javascript
     switch (day) {
       case 'Monday':
         console.log('Start of the workweek.');
         break;
       case 'Friday':
         console.log('Weekend is near!');
         break;
       default:
         console.log('It\'s a regular day.');
     }
     ```

---

## Summary
- Use `if`, `else if`, and `else` for conditional logic.
- Use comparison operators (`<`, `>`, `===`, etc.) to compare values.
- Use logical operators (`&&`, `||`, `!`) to combine or negate conditions.
- Simplify code with the **ternary operator** and **`switch` statements**.

---

## Example
```javascript
const age = 20;
const day = 'Saturday';

if (age >= 18) {
  console.log('You are an adult.');
} else {
  console.log('You are a minor.');
}

if (day === 'Saturday' || day === 'Sunday') {
  console.log('It\'s the weekend!');
} else {
  console.log('It\'s a workday.');
}

const isRaining = false;
console.log(!isRaining ? 'Enjoy the sunshine!' : 'Grab an umbrella!');

switch (day) {
  case 'Monday':
    console.log('Start of the workweek.');
    break;
  case 'Friday':
    console.log('Weekend is near!');
    break;
  default:
    console.log('It\'s a regular day.');
}

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

# Scope in JavaScript - Review

## Key Concepts
1. **Scope**:
   - Determines where variables can be accessed in a program.
   - Depends on where and how variables are declared.

2. **Blocks**:
   - Statements enclosed in curly braces `{}`.
   - Example:
     ```javascript
     if (true) {
       // This is a block
     }
     ```

3. **Global Scope**:
   - Variables declared outside of any block or function.
   - Accessible everywhere in the program.
   - Example:
     ```javascript
     const globalVar = 'I am global!';
     function checkScope() {
       console.log(globalVar); // Accessible
     }
     ```

4. **Global Variables**:
   - Variables declared in the global scope.
   - Example:
     ```javascript
     let globalVar = 'I am a global variable';
     ```

5. **Block Scope**:
   - Variables declared inside a block `{}` are only accessible within that block.
   - Introduced in ES6 with `let` and `const`.
   - Example:
     ```javascript
     if (true) {
       const blockVar = 'I am block-scoped';
       console.log(blockVar); // Accessible
     }
     console.log(blockVar); // Error: blockVar is not defined
     ```

6. **Local Variables**:
   - Variables declared within a block or function.
   - Accessible only within that block or function.
   - Example:
     ```javascript
     function myFunction() {
       const localVar = 'I am local!';
       console.log(localVar); // Accessible
     }
     console.log(localVar); // Error: localVar is not defined
     ```

7. **Global Namespace**:
   - The space in code that contains globally scoped information.
   - Example:
     ```javascript
     const globalVar = 'I am in the global namespace';
     ```

8. **Scope Pollution**:
   - Occurs when too many variables exist in the global namespace or variable names are reused.
   - Can lead to bugs and conflicts.
   - Best Practice: Avoid polluting the global scope by using block-scoped variables (`let` and `const`).

---

## Best Practices for Scope
- Use `let` and `const` instead of `var` to avoid unintended global variables.
- Declare variables in the smallest scope possible.
- Avoid reusing variable names in nested scopes.
- Minimize the use of global variables to prevent scope pollution.

---

## Example Code
```javascript
// Global Scope
const globalVar = 'I am global!';

function checkScope() {
  // Function Scope
  const localVar = 'I am local!';
  console.log(globalVar); // Accessible
  console.log(localVar);  // Accessible

  if (true) {
    // Block Scope
    const blockVar = 'I am block-scoped!';
    console.log(blockVar); // Accessible
  }
  console.log(blockVar); // Error: blockVar is not defined
}

console.log(globalVar); // Accessible
console.log(localVar);  // Error: localVar is not defined

# Arrays in JavaScript - Review

## Key Concepts
1. **What is an Array?**
   - A list that stores data in JavaScript.
   - Created with square brackets `[]`.
   - Example:
     ```javascript
     const fruits = ['apple', 'banana', 'cherry'];
     ```

2. **Array Indexing**:
   - Each item in an array has a numbered position (index), starting at `0`.
   - Access an item using its index: `myArray[index]`.
   - Example:
     ```javascript
     console.log(fruits[0]); // 'apple'
     ```

3. **Modifying Arrays**:
   - Change an item using its index: `myArray[index] = newValue`.
   - Example:
     ```javascript
     fruits[1] = 'blueberry';
     console.log(fruits); // ['apple', 'blueberry', 'cherry']
     ```

4. **Array Length**:
   - Use the `length` property to see how many items are in an array.
   - Example:
     ```javascript
     console.log(fruits.length); // 3
     ```

5. **Array Methods**:
   - **`.push()`**: Adds an item to the end of an array.
     ```javascript
     fruits.push('date');
     console.log(fruits); // ['apple', 'blueberry', 'cherry', 'date']
     ```
   - **`.pop()`**: Removes the last item from an array.
     ```javascript
     fruits.pop();
     console.log(fruits); // ['apple', 'blueberry', 'cherry']
     ```
   - **`.shift()`**: Removes the first item from an array.
     ```javascript
     fruits.shift();
     console.log(fruits); // ['blueberry', 'cherry']
     ```
   - **`.slice()`**: Returns a new array with a portion of the original array.
     ```javascript
     const newFruits = fruits.slice(0, 1);
     console.log(newFruits); // ['blueberry']
     ```

6. **Mutating vs. Non-Mutating Methods**:
   - **Mutating**: Changes the original array (e.g., `.push()`, `.pop()`, `.shift()`).
   - **Non-Mutating**: Returns a new array without changing the original (e.g., `.slice()`).

7. **Variables and Arrays**:
   - Arrays can be declared with `let` or `const`.
   - Arrays declared with `const` are still mutable, but the variable cannot be reassigned.
   - Example:
     ```javascript
     const colors = ['red', 'green'];
     colors.push('blue'); // Allowed
     colors = ['yellow']; // Error: Assignment to constant variable.
     ```

8. **Arrays in Functions**:
   - Arrays mutated inside a function retain those changes outside the function.
   - Example:
     ```javascript
     function addFruit(arr, fruit) {
       arr.push(fruit);
     }
     addFruit(fruits, 'date');
     console.log(fruits); // ['blueberry', 'cherry', 'date']
     ```

9. **Nested Arrays**:
   - Arrays can contain other arrays.
   - Access elements in nested arrays using chained indices.
   - Example:
     ```javascript
     const nestedArray = [[1, 2], [3, 4]];
     console.log(nestedArray[1][0]); // 3
     ```

---

## Example Code
```javascript
// Creating an array
const fruits = ['apple', 'banana', 'cherry'];

// Accessing elements
console.log(fruits[0]); // 'apple'

// Modifying elements
fruits[1] = 'blueberry';
console.log(fruits); // ['apple', 'blueberry', 'cherry']

// Array length
console.log(fruits.length); // 3

// Adding and removing elements
fruits.push('date');
console.log(fruits); // ['apple', 'blueberry', 'cherry', 'date']
fruits.pop();
console.log(fruits); // ['apple', 'blueberry', 'cherry']

// Nested arrays
const nestedArray = [[1, 2], [3, 4]];
console.log(nestedArray[1][0]); // 3

# Loops in JavaScript - Review

## Key Concepts
1. **What are Loops?**
   - Loops perform repetitive actions, eliminating the need to manually repeat code.
   - Example:
     ```javascript
     for (let i = 0; i < 5; i++) {
       console.log(i); // Prints 0, 1, 2, 3, 4
     }
     ```

2. **`for` Loops**:
   - Use an iterator variable to increment or decrement.
   - Commonly used to iterate through arrays.
   - Example:
     ```javascript
     const fruits = ['apple', 'banana', 'cherry'];
     for (let i = 0; i < fruits.length; i++) {
       console.log(fruits[i]);
     }
     ```

3. **Nested `for` Loops**:
   - A loop inside another loop.
   - Example:
     ```javascript
     for (let i = 0; i < 3; i++) {
       for (let j = 0; j < 2; j++) {
         console.log(`i: ${i}, j: ${j}`);
       }
     }
     ```

4. **`while` Loops**:
   - Execute code as long as a condition is true.
   - Useful when the number of iterations is unknown.
   - Example:
     ```javascript
     let count = 0;
     while (count < 5) {
       console.log(count);
       count++;
     }
     ```

5. **Stopping Conditions**:
   - Crucial for preventing infinite loops.
   - Example:
     ```javascript
     let x = 0;
     while (x < 10) {
       console.log(x);
       x++; // Ensures the loop eventually stops
     }
     ```

6. **`do...while` Loops**:
   - Execute code at least once, then check the stopping condition.
   - Example:
     ```javascript
     let y = 0;
     do {
       console.log(y);
       y++;
     } while (y < 5);
     ```

7. **`break` Keyword**:
   - Exits a loop immediately.
   - Example:
     ```javascript
     for (let i = 0; i < 10; i++) {
       if (i === 5) {
         break; // Stops the loop when i is 5
       }
       console.log(i);
     }
     ```

---

## Example Code
```javascript
// for Loop
for (let i = 0; i < 3; i++) {
  console.log(`For loop iteration: ${i}`);
}

// while Loop
let count = 0;
while (count < 3) {
  console.log(`While loop iteration: ${count}`);
  count++;
}

// do...while Loop
let x = 0;
do {
  console.log(`Do...while loop iteration: ${x}`);
  x++;
} while (x < 3);

// Nested for Loop
for (let i = 0; i < 2; i++) {
  for (let j = 0; j < 2; j++) {
    console.log(`Nested loop: i=${i}, j=${j}`);
  }
}

// break Keyword
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    break; // Exits the loop when i is 3
  }
  console.log(`Break example: ${i}`);
}

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

# Iterators in JavaScript - Review

## Key Concepts
1. **Iterator Methods**:
   - These methods allow you to perform operations on arrays in a clean and functional way.
   - All iterator methods take a **callback function** as an argument, which can be:
     - A pre-defined function.
     - A function expression.
     - An arrow function.

2. **`.forEach()`**:
   - Executes the same code on every element in an array.
   - Does **not change the array** and returns `undefined`.
   - Example:
     ```javascript
     const numbers = [1, 2, 3];
     numbers.forEach(num => console.log(num * 2));
     // Output: 2, 4, 6
     ```

3. **`.map()`**:
   - Executes the same code on every element in an array.
   - Returns a **new array** with the updated elements.
   - Example:
     ```javascript
     const doubled = numbers.map(num => num * 2);
     console.log(doubled); // [2, 4, 6]
     ```

4. **`.filter()`**:
   - Checks every element in an array to see if it meets certain criteria.
   - Returns a **new array** with elements that satisfy the condition.
   - Example:
     ```javascript
     const evens = numbers.filter(num => num % 2 === 0);
     console.log(evens); // [2]
     ```

5. **`.findIndex()`**:
   - Returns the **index** of the first element that satisfies a condition.
   - Returns `-1` if no elements satisfy the condition.
   - Example:
     ```javascript
     const index = numbers.findIndex(num => num > 2);
     console.log(index); // 2
     ```

6. **`.reduce()`**:
   - Iterates through an array and accumulates values into a **single result**.
   - Example:
     ```javascript
     const sum = numbers.reduce((accumulator, num) => accumulator + num, 0);
     console.log(sum); // 6
     ```

---

## Example Code
```javascript
const numbers = [1, 2, 3];

// .forEach()
numbers.forEach(num => console.log(num * 2));
// Output: 2, 4, 6

// .map()
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6]

// .filter()
const evens = numbers.filter(num => num % 2 === 0);
console.log(evens); // [2]

// .findIndex()
const index = numbers.findIndex(num => num > 2);
console.log(index); // 2

// .reduce()
const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // 6

# Objects in JavaScript - Review

## Key Concepts
1. **What are Objects?**
   - Objects store collections of **key-value pairs**.
   - Used to organize data and model real-world entities.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       age: 25,
     };
     ```

2. **Properties and Methods**:
   - **Property**: A key-value pair in an object.
   - **Method**: A property whose value is a function.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       greet: function() {
         console.log(`Hello, my name is ${this.name}`);
       },
     };
     person.greet(); // "Hello, my name is Alice"
     ```

3. **Object Literals**:
   - Created using curly braces `{}` with comma-separated key-value pairs.
   - Example:
     ```javascript
     const car = {
       make: 'Toyota',
       model: 'Corolla',
       year: 2020,
     };
     ```

4. **Accessing and Modifying Properties**:
   - Use **dot notation** or **bracket notation**.
   - Example:
     ```javascript
     console.log(car.make); // "Toyota" (dot notation)
     console.log(car['model']); // "Corolla" (bracket notation)
     car.year = 2021; // Modify a property
     ```

5. **Adding Methods**:
   - Use anonymous functions or ES6 method syntax.
   - Example:
     ```javascript
     const car = {
       make: 'Toyota',
       drive: function() {
         console.log('Vroom!');
       },
       // ES6 method syntax
       honk() {
         console.log('Beep!');
       },
     };
     car.drive(); // "Vroom!"
     car.honk(); // "Beep!"
     ```

6. **Nested Objects**:
   - Objects can contain other objects.
   - Use chaining to access nested properties.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       address: {
         city: 'New York',
         zip: '10001',
       },
     };
     console.log(person.address.city); // "New York"
     ```

7. **Mutability**:
   - Objects are mutable, even when declared with `const`.
   - Example:
     ```javascript
     const person = { name: 'Alice' };
     person.name = 'Bob'; // Allowed
     ```

8. **Passed by Reference**:
   - Objects are passed by reference, meaning changes to an object inside a function persist outside the function.
   - Example:
     ```javascript
     function updateName(obj) {
       obj.name = 'Charlie';
     }
     updateName(person);
     console.log(person.name); // "Charlie"
     ```

9. **Iterating Through Objects**:
   - Use `for...in` to loop through object properties.
   - Example:
     ```javascript
     for (let key in person) {
       console.log(`${key}: ${person[key]}`);
     }
     // Output:
     // name: Charlie
     // address: [object Object]
     ```

---

## Example Code
```javascript
// Object Literal
const person = {
  name: 'Alice',
  age: 25,
  address: {
    city: 'New York',
    zip: '10001',
  },
  greet() {
    console.log(`Hello, my name is ${this.name}`);
  },
};

// Accessing Properties
console.log(person.name); // "Alice"
console.log(person['age']); // 25

// Modifying Properties
person.age = 26;
console.log(person.age); // 26

// Adding Methods
person.sayAge = function() {
  console.log(`I am ${this.age} years old.`);
};
person.sayAge(); // "I am 26 years old."

// Iterating Through Objects
for (let key in person) {
  console.log(`${key}: ${person[key]}`);
}
// Output:
// name: Alice
// age: 26
// address: [object Object]
// greet: function greet() { ... }
// sayAge: function () { ... }

# Advanced Objects in JavaScript - Review

## Key Concepts
1. **Calling Object**:
   - The object that a method belongs to is called the **calling object**.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       greet() {
         console.log(`Hello, my name is ${this.name}`);
       },
     };
     person.greet(); // "Hello, my name is Alice"
     ```

2. **`this` Keyword**:
   - Refers to the **calling object** and is used to access its properties.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       greet() {
         console.log(`Hello, my name is ${this.name}`);
       },
     };
     person.greet(); // "Hello, my name is Alice"
     ```

3. **Accessing Internal Properties**:
   - Methods do not automatically have access to other internal properties unless explicitly referenced using `this`.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       age: 25,
       greet() {
         console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
       },
     };
     person.greet(); // "Hello, my name is Alice and I am 25 years old."
     ```

4. **Value of `this`**:
   - The value of `this` depends on the context in which it is accessed.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       greet: () => {
         console.log(`Hello, my name is ${this.name}`);
       },
     };
     person.greet(); // "Hello, my name is undefined" (arrow function does not bind `this`)
     ```

5. **Arrow Functions as Methods**:
   - Arrow functions should not be used as methods if you need to access other internal properties using `this`.
   - Example:
     ```javascript
     const person = {
       name: 'Alice',
       greet: function() {
         console.log(`Hello, my name is ${this.name}`);
       },
     };
     person.greet(); // "Hello, my name is Alice"
     ```

6. **Privacy in Objects**:
   - JavaScript objects do not have built-in privacy.
   - Use an **underscore** (`_`) before a property name to indicate that it should not be directly modified.
   - Example:
     ```javascript
     const person = {
       _name: 'Alice',
       getName() {
         return this._name;
       },
     };
     console.log(person.getName()); // "Alice"
     ```

7. **Setters and Getters**:
   - Allow for controlled access and assignment of properties.
   - Example:
     ```javascript
     const person = {
       _name: 'Alice',
       get name() {
         return this._name;
       },
       set name(newName) {
         this._name = newName;
       },
     };
     person.name = 'Bob';
     console.log(person.name); // "Bob"
     ```

8. **Factory Functions**:
   - Functions that create and return object instances quickly and repeatedly.
   - Example:
     ```javascript
     function createPerson(name, age) {
       return {
         name,
         age,
         greet() {
           console.log(`Hello, my name is ${this.name}`);
         },
       };
     }
     const alice = createPerson('Alice', 25);
     alice.greet(); // "Hello, my name is Alice"
     ```

9. **Object Destructuring**:
   - **Property Value Shorthand**: Simplifies object creation.
     ```javascript
     const name = 'Alice';
     const age = 25;
     const person = { name, age };
     console.log(person); // { name: 'Alice', age: 25 }
     ```
   - **Destructured Assignment**: Extracts properties into variables.
     ```javascript
     const { name, age } = person;
     console.log(name); // "Alice"
     console.log(age); // 25
     ```

---

## Example Code
```javascript
// Using `this` in Methods
const person = {
  name: 'Alice',
  greet() {
    console.log(`Hello, my name is ${this.name}`);
  },
};
person.greet(); // "Hello, my name is Alice"

// Privacy Convention
const account = {
  _balance: 1000,
  get balance() {
    return this._balance;
  },
  set balance(amount) {
    this._balance = amount;
  },
};
account.balance = 1500;
console.log(account.balance); // 1500

// Factory Function
function createPerson(name, age) {
  return {
    name,
    age,
    greet() {
      console.log(`Hello, my name is ${this.name}`);
    },
  };
}
const bob = createPerson('Bob', 30);
bob.greet(); // "Hello, my name is Bob"

// Object Destructuring
const { name, age } = bob;
console.log(name); // "Bob"
console.log(age); // 30