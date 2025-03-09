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