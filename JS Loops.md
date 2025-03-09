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