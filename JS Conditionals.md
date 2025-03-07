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