Here’s your improved and complete version with **Learning Objectives** at the start and a clear **Conclusion** at the end 👇

---

## 🧠 **Student Notes: Let’s Reuse Code – Functions That Work for You**

---

### 🎯 **Learning Objectives**

By the end of this session, you will be able to:

1. Understand what a function is and why it’s needed.
2. Write and use functions effectively in JavaScript.
3. Differentiate between **function declarations** and **function expressions**.
4. Use **parameters**, **arguments**, and **default values** in functions.
5. Understand how **return statements** work.
6. Grasp the concept of **hoisting** and **scope**.
7. Apply **best practices** to write clean, reusable, and modular code.

---

### **1. Brief Revision of Previous Session**

* Arrays and strings simplify data handling in programming.
* Functions are another tool to make programming efficient and reusable by reducing repetitive code.

---

### **2. What Is a Function and Why Is It Needed?**

* **Definition:** A function is a reusable block of code designed to perform a specific task.
* **Why Use Functions?**

  1. Avoid repetitive code.
  2. Enhance readability and maintainability.
  3. Make code modular, allowing reuse across programs.

**Example Without a Function:**

```javascript
console.log(5 + 3);
console.log(10 + 3);
console.log(15 + 3);
```

**Example With a Function:**

```javascript
function addThree(num) {
  console.log(num + 3);
}
addThree(5);  // Outputs 8
addThree(10); // Outputs 13
addThree(15); // Outputs 18
```

---

### **3. Function Declarations and Expressions**

* **Function Declaration:**
  A function defined with a name and called later.

**Example:**

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}
greet("Alice"); // Outputs: Hello, Alice!
```

* **Function Expression:**
  A function assigned to a variable and used as a value.

**Example:**

```javascript
const greet = function(name) {
  console.log(`Hello, ${name}!`);
};
greet("Bob"); // Outputs: Hello, Bob!
```

* **Key Difference:** Declarations are hoisted (explained in Hoisting), but expressions are not.

---

### **4. Parameters and Arguments**

* **Parameters:** Placeholder variables defined in the function definition.
* **Arguments:** Actual values passed when the function is called.
* **Default Parameters:** Provide fallback values when no arguments are passed.

**Example:**

```javascript
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}
greet();          // Outputs: Hello, Guest!
greet("Charlie"); // Outputs: Hello, Charlie!
```

---

### **5. Return Statements**

* Functions can return values using the `return` keyword.
* Use `return` to send data back to the caller.

**Example:**

```javascript
function square(num) {
  return num * num;
}
let result = square(4);
console.log(result); // Outputs 16
```

---

### **6. Hoisting and Scoping of Variables**

#### **Hoisting:**

* JavaScript moves declarations to the top of the scope during execution.
* **Function Declarations:** Fully hoisted.
* **Variable Declarations with `var`:** Hoisted but not initialized.
* **`let` and `const`:** Hoisted but remain in a **temporal dead zone** until initialized.

**Example:**

```javascript
console.log(a); // Outputs undefined
var a = 10;

// console.log(b); // ReferenceError
let b = 20;
```

#### **Scope:**

* **Global Scope:** Accessible throughout the program.
* **Local Scope:** Available only inside the function or block it is declared in.

**Example:**

```javascript
let globalVar = "I am global";

function exampleScope() {
  let localVar = "I am local";
  console.log(globalVar); // Accessible
  console.log(localVar);  // Accessible
}
exampleScope();
console.log(localVar); // Error: localVar is not defined
```

---

### **7. Best Practices**

1. **Use Descriptive Names:** Choose meaningful names for functions.

   * Good: `calculateSum()`
   * Bad: `cs()`
2. **Keep Functions Small:** Each function should perform a single task.
3. **Avoid Repetition:** Use functions to handle repetitive code.

---

### **Examples**

**Task 1: Greeting Function with Default Parameters**

```javascript
function greetUser(name, timeOfDay = "day") {
  console.log(`Good ${timeOfDay}, ${name}!`);
}
greetUser("Alice", "morning"); // Outputs: Good morning, Alice!
greetUser("Bob");             // Outputs: Good day, Bob!
```

**Task 2: Array Manipulation with a Function**

```javascript
function doubleArray(numbers) {
  return numbers.map(num => num * 2);
}
let arr = [1, 2, 3];
console.log(doubleArray(arr)); // Outputs: [2, 4, 6]
```

**Task 3: Arithmetic Operations**

```javascript
function calculate(a, b, operation) {
  if (operation === "add") return a + b;
  if (operation === "subtract") return a - b;
  if (operation === "multiply") return a * b;
  if (operation === "divide") return a / b;
  return "Invalid operation";
}
console.log(calculate(10, 5, "add")); // Outputs 15
```

---

### **Combination of All Concepts**

**Problem Statement:**
Create a function to calculate the total cost of items in a cart, apply a discount, and return the final amount.

**Solution:**

```javascript
function calculateCartTotal(items, discount) {
  let total = 0;
  for (let price of items) {
    total += price;
  }
  let discountedTotal = total - (total * discount / 100);
  return discountedTotal;
}

let cart = [100, 200, 300];
let discount = 10; // 10% discount
console.log(`Final Amount: Rs. ${calculateCartTotal(cart, discount)}`);
// Outputs: Final Amount: Rs. 540
```

This function combines loops, parameters, arguments, and return statements to solve a practical problem.

---

### 🏁 **Conclusion**

* Functions are **the building blocks of modular programming**.
* They help in **reusing**, **organizing**, and **maintaining** code efficiently.
* Understanding **parameters, return values, and scope** helps you write cleaner and more effective programs.
* Always follow **best practices**: keep functions focused, name them clearly, and avoid duplication.


---

