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