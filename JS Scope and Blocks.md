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