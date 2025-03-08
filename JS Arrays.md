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