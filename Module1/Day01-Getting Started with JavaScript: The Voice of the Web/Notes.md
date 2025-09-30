PPT Used in the Class

[Getting Started with JS](https://coding-platform.s3.amazonaws.com/dev/lms/tickets/bc39ea29-436a-441a-928d-7c3c45a9e77c/oSMKPaojjzcidmVI.pdf)

### **Getting Started with JavaScript: The Voice of the Web**

---

### **Student Notes**

---

### **1. Introduction to JavaScript**

**What is JavaScript?**  
JavaScript is a lightweight, interpreted programming language primarily used to make web pages interactive. It is one of the core technologies of web development alongside HTML and CSS.

**Key Points**:

- **Dynamic Language**: JavaScript adds behavior and interactivity to web pages.
- **High-Level**: Abstracts many of the complexities of low-level programming.
- **Event-Driven**: Can respond to user actions like clicks, typing, and scrolling.
- **Cross-Platform**: Runs in any modern browser without additional software.

**Evolution of JavaScript**:

- **1995**: Developed by Brendan Eich in 10 days.
- **1997**: Standardized as ECMAScript (ES).
- **2015 (ES6)**: Major update introducing modern features like `let`, `const`, arrow functions, and classes.
- Today: JavaScript powers client-side and server-side applications, mobile apps, games, and more.

**Why is JavaScript Important in Web Development?**

- Enables **dynamic content** (e.g., updating without refreshing the page).
- Adds **interactivity** (e.g., buttons, sliders, forms).
- Supports modern tools and libraries like React, Angular, and Node.js.

---

### **2. JavaScript Syntax Essentials**

#### (Demonstration using [One Complier](https://onecompiler.com/javascript) link for JS for now, show them creating different files for day to day activities also sharing access to be public)

**What is Syntax?**  
Syntax refers to the set of rules for writing valid JavaScript code.

**Basic Syntax Rules**:

- **Case Sensitive**: `myVariable` and `myvariable` are different.
- **Statements**: Code instructions that perform an action. End with a semicolon (`;`) (optional but recommended).
- **Whitespace**: Ignored by JavaScript, but use it to make code readable.

**Comments in JavaScript**:

- **Single-line comments**: Use `//` to write comments on a single line.
  ```javascript
  // This is a single-line comment.
  ```
- **Multi-line comments**: Use `/* */` for longer comments.
  ```javascript
  /*
  This is a multi-line comment.
  Useful for detailed explanations.
  */
  ```

**Example**:

```javascript
let message = "Hello, World!"; // This is a statement.
console.log(message); // Prints: Hello, World!
```

---

### **3. Variables and Constants**

**What are Variables?**  
Variables are used to store data values in memory.

**Declaring Variables**:

- Use `let` or `const` (modern JavaScript).
- Avoid `var` due to scoping issues in older JavaScript.

**Constants**:

- Use `const` for values that will not change.

**Rules for Naming Variables**:

- Must start with a letter, `$`, or `_`.
- Cannot include spaces or special characters (except `$` and `_`).
- Should not use reserved keywords like `if`, `let`, or `const`.
- Use camelCase for readability: `myVariableName`.

**Example**:

```javascript
let userName = "Alice"; // Declares a variable with let.
const birthYear = 2000; // Declares a constant with const.
console.log(userName, birthYear); // Outputs: Alice 2000.
```

---

#### **4. Data Types in JavaScript**

**What are Data Types?**  
Data types define the kind of data a variable can hold.

**Primitive Data Types**:

1. **String**: Textual data enclosed in quotes (`' '`, `" "`, or `` ` ` `).
   ```javascript
   let name = "John";
   console.log(name); // Outputs: John
   ```
2. **Number**: Integers and floating-point numbers.
   ```javascript
   let age = 25;
   console.log(age); // Outputs: 25
   ```
3. **Boolean**: Logical values `true` or `false`.
   ```javascript
   let isStudent = true;
   console.log(isStudent); // Outputs: true
   ```
4. **null**: Explicitly represents "no value."
   ```javascript
   let emptyValue = null;
   console.log(emptyValue); // Outputs: null
   ```
5. **undefined**: Represents a variable declared but not assigned a value.
   ```javascript
   let notAssigned;
   console.log(notAssigned); // Outputs: undefined
   ```

**Dynamic Typing**:  
JavaScript variables can hold any type of value, and the type can change during execution.

**Example**:

```javascript
let variable = "Hello";
console.log(variable); // Outputs: Hello
variable = 100;
console.log(variable); // Outputs: 100
```

---

### **5. String Concatenation**

**What is String Concatenation?**  
Combining two or more strings into one.

**Methods**:

1. **Using `+` Operator**:
   ```javascript
   let firstName = "Jane";
   let lastName = "Doe";
   console.log("Hello, " + firstName + " " + lastName); // Outputs: Hello, Jane Doe
   ```
2. **Using Template Literals** (Preferred):
   - Use backticks `` ` `` for strings and `${expression}` for embedding variables.
   ```javascript
   console.log(`Hello, ${firstName} ${lastName}`); // Outputs: Hello, Jane Doe
   ```

---

### **6. Type Coercion**

**What is Type Coercion?**  
JavaScript automatically converts one data type to another when required.

**Types of Coercion**:

1. **Implicit Coercion**: Happens automatically.
   ```javascript
   console.log("5" + 2); // Outputs: 52 (string concatenation)
   console.log("5" - 2); // Outputs: 3 (number subtraction)
   ```
2. **Explicit Conversion**: Done manually using functions like `Number()`, `String()`, or `Boolean()`.

   ```javascript
   let num = Number("10");
   console.log(num + 5); // Outputs: 15

   let str = String(100);
   console.log(str + " is a string."); // Outputs: 100 is a string.
   ```

---

### **7. Basic Output**

**What is `console.log()`?**

- A method used to print messages or variable values to the browser console for debugging or testing.

**Example**:

```javascript
let greeting = "Welcome to JavaScript!";
console.log(greeting); // Outputs: Welcome to JavaScript!
```

---

### **8. Debugging Basics**

**Why Debug?**

- Debugging helps identify and fix issues in code.

**Using `console.log()`**:

- Print variable values to track their state.
- Identify unexpected outputs during code execution.

**Example**:

```javascript
let a = 10;
let b = 20;
console.log("Value of a:", a); // Outputs: Value of a: 10
console.log("Value of b:", b); // Outputs: Value of b: 20
console.log("Sum:", a + b); // Outputs: Sum: 30
```

---

### **Hands-On Activities**

---

#### **Hands-On Activities – Day 1**

1. **Activity 1**:

   - Declare variables for a person’s name, birth year, and hobby.
   - Calculate their age and display:
     `"Hi [name], you are [age] years old and love [hobby]."`

**Solution**:

```javascript
let name = "Alice";
let birthYear = 1995;
let hobby = "painting";
let currentYear = 2024;

let age = currentYear - birthYear;
console.log(`Hi ${name}, you are ${age} years old and love ${hobby}.`);
```

---

2. **Activity 2**:

   - Demonstrate type coercion using string and number operations.

**Solution**:

```javascript
let num = 10;
let str = "5";

console.log(num + str); // Outputs: 105 (string concatenation)
console.log(num - str); // Outputs: 5 (number subtraction)
```

---

3. **Activity 3**:

   - Declare three variables for items (`item1`, `item2`, `item3`) with values `"Rice"`, `"Dal"`, and `"Oil"`.
   - Declare their prices (`price1`, `price2`, `price3`).
   - Ask for customer name and print a **fun shopping bill** with:

     - Greeting message
     - Simple bill table
     - Grand total
     - Closing “Thank You” message

   - Use emojis for better design

**Solution**:

```javascript
let customerName = "John";

let item1 = "Rice";
let item2 = "Dal";
let item3 = "Oil";

let price1 = 50;
let price2 = 80;
let price3 = 120;

let total = price1 + price2 + price3;

console.log(`👋 Hello Mr/Ms ${customerName}, thanks for shopping with us! 🛍️`);
console.log("====== 🧾 Simple Bill ======");
console.log("Sl No | Item   | Price");
console.log("----------------------------");
console.log(`1     | ${item1}   | ${price1}`);
console.log(`2     | ${item2}    | ${price2}`);
console.log(`3     | ${item3}    | ${price3}`);
console.log("----------------------------");
console.log(`💰 Grand Total: ${total}`);
console.log("----------------------------");
console.log("🙏 Thanks and Visit Again! 😊");
```

**Output (example):**

```
👋 Hello Mr/Ms John, thanks for shopping with us! 🛍️
====== 🧾 Simple Bill ======
Sl No | Item   | Price
----------------------------
1     | Rice   | 50
2     | Dal    | 80
3     | Oil    | 120
----------------------------
💰 Grand Total: 250
----------------------------
🙏 Thanks and Visit Again! 😊
```

---
