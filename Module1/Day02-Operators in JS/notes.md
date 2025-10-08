PPT Link Used Today: 

[Operators in JS](https://coding-platform.s3.amazonaws.com/dev/lms/tickets/9f3f5ea8-db43-4879-830f-bea0a72ffb41/dhGfnBUKeNixGh3u.pdf)

### Student Notes: 
## Mastering Operators – Math, Logic, Comparisons, and Conditionals


---

### **1. Arithmetic Operators**

#### **Overview:**
Arithmetic operators are used to perform mathematical operations.

| **Operator** | **Description**       | **Example**             | **Output** |
|--------------|-----------------------|-------------------------|------------|
| `+`          | Addition              | `5 + 2`                 | `7`        |
| `-`          | Subtraction           | `5 - 2`                 | `3`        |
| `*`          | Multiplication        | `5 * 2`                 | `10`       |
| `/`          | Division              | `5 / 2`                 | `2.5`      |
| `%`          | Modulus (Remainder)   | `5 % 2`                 | `1`        |

#### **Code Examples:**

```javascript
let sum = 10 + 5; // 15
let difference = 10 - 5; // 5
let product = 10 * 2; // 20
let quotient = 10 / 2; // 5
let remainder = 10 % 3; // 1
console.log(sum, difference, product, quotient, remainder);
```

---

### **2. Logical Operators**

#### **Overview:**
Logical operators are used to combine conditional expressions.

| **Operator** | **Description**    | **Example**                  | **Output** |
|--------------|--------------------|------------------------------|------------|
| `&&`         | Logical AND        | `(true && false)`            | `false`    |
| ll         | Logical OR         | (true ll false)            | `true`     |
| `!`          | Logical NOT        | `!(true)`                    | `false`    |

#### **Code Examples:**

```javascript
let age = 20;
let isAdult = age > 18 && age < 60; // true
let isTeenager = age < 18 || age === 18; // false
let notTeenager = !isTeenager; // true
console.log(isAdult, isTeenager, notTeenager);
```

---

### **3. Comparison Operators**

#### **Overview:**
Comparison operators are used to compare values and return a boolean (`true` or `false`).

| **Operator** | **Description**             | **Example**           | **Output** |
|--------------|-----------------------------|-----------------------|------------|
| `>`          | Greater than                | `5 > 3`               | `true`     |
| `<`          | Less than                   | `5 < 3`               | `false`    |
| `>=`         | Greater than or equal to    | `5 >= 5`              | `true`     |
| `<=`         | Less than or equal to       | `5 <= 4`              | `false`    |
| `==`         | Equality (loose comparison) | `5 == "5"`            | `true`     |
| `===`        | Equality (strict comparison)| `5 === "5"`           | `false`    |
| `!=`         | Inequality (loose)          | `5 != "5"`            | `false`    |
| `!==`        | Inequality (strict)         | `5 !== "5"`           | `true`     |

#### **Code Examples:**

```javascript
console.log(5 > 3);  // true
console.log(5 === "5"); // false
console.log(10 <= 20); // true
console.log(5 !== 6); // true
```

---

### **4. Operator Precedence**

#### **Overview:**
Operator precedence determines the order in which operators are evaluated in expressions. Higher precedence operators execute before lower precedence ones.

#### **Precedence Table:**

| **Precedence** | **Operator**             | **Description**                     | **Associativity**   |
|----------------|--------------------------|-------------------------------------|---------------------|
| **1**          | `()`                     | Parentheses (Grouping)              | Left-to-Right       |
| **2**          | `++`, `--`               | Increment, Decrement                | Right-to-Left       |
| **3**          | `*`, `/`, `%`            | Multiplication, Division, Modulus   | Left-to-Right       |
| **4**          | `+`, `-`                 | Addition, Subtraction               | Left-to-Right       |
| **5**          | `<`, `<=`, `>`, `>=`     | Relational Operators                | Left-to-Right       |
| **6**          | `==`, `!=`, `===`, `!==` | Equality Operators                  | Left-to-Right       |
| **7**          | `&&`                     | Logical AND                         | Left-to-Right       |
| **8**          |   ll                    | Logical OR                          | Left-to-Right       |
| **9**          | `=`                      | Assignment                          | Right-to-Left       |

#### **Code Examples:**

1. **Basic Precedence Example:**

```javascript
let result = 10 + 5 * 2; 
console.log(result); // Output: 20 (Multiplication is performed first)
```

2. **Using Parentheses to Change Precedence:**

```javascript
let result = (10 + 5) * 2; 
console.log(result); // Output: 30 (Addition is performed first due to parentheses)
```

---

### **5. Conditional Statements**

#### **Overview:**
Conditional statements control the flow of the program based on conditions.

#### **Syntax:**

```javascript
if (condition) {
  // Code to execute if condition is true
} else if (anotherCondition) {
  // Code to execute if anotherCondition is true
} else {
  // Code to execute if all conditions are false
}
```

#### **Code Example:**

```javascript
let age = 20;

if (age < 18) {
  console.log("You are a minor.");
} else if (age >= 18 && age < 60) {
  console.log("You are an adult.");
} else {
  console.log("You are a senior.");
}
```

---

### **6. Combining All Operators and Statements**

#### **Example Scenario:**
Using arithmetic, logical, comparison operators, and conditionals to evaluate and execute logic.

```javascript
let price = 150;
let discount = 20;
let finalPrice = price - discount;
let isAffordable = finalPrice <= 100;

if (isAffordable && finalPrice > 50) {
  console.log("The item is affordable and worth buying!");
} else if (!isAffordable) {
  console.log("The item is too expensive.");
} else {
  console.log("Consider buying something else.");
}
```

---

### **7. Problem Statement and Solution**

#### **Problem:**
Write a program that takes the current hour (in 24-hour format) and decides if it's morning, afternoon, evening, or night. It should also calculate the time remaining for the next part of the day.

#### **Solution:**

```javascript
let hour = 14; // Current time: 2 PM

if (hour >= 6 && hour < 12) {
  console.log("Good Morning!");
  console.log(`Hours left for afternoon: ${12 - hour}`);
} else if (hour >= 12 && hour < 18) {
  console.log("Good Afternoon!");
  console.log(`Hours left for evening: ${18 - hour}`);
} else if (hour >= 18 && hour < 22) {
  console.log("Good Evening!");
  console.log(`Hours left for night: ${22 - hour}`);
} else {
  console.log("Good Night!");
  console.log(`Hours left for morning: ${6 - (hour > 22 ? 24 : hour)}`);
}
```

---