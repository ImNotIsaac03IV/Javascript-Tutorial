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