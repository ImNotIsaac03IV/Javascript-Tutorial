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