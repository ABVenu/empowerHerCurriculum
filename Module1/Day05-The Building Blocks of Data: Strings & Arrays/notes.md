### **Student Notes: Arrays & Strings**

---

#### **1. Introduction to Array and String Data Types and Their Needs**

##### **What Is an Array?**  
An **array** is a collection of elements, such as numbers, strings, or objects, stored in a single variable. Each element is assigned an **index**, starting from `0`. Arrays provide a way to organize and manage data efficiently, especially when dealing with a list of related items.  

**Why Are Arrays Needed in Programming?**  
- To handle a collection of data without needing separate variables for each element.  
- To easily access, update, and manipulate related data.  
- To simplify repetitive tasks, such as applying the same operation to multiple values.

**Example:**  
```javascript
// Storing multiple numbers in an array
let scores = [85, 90, 78, 88];
console.log(scores); // Output: [85, 90, 78, 88]
```

##### **What Is a String?**  
A **string** is a sequence of characters enclosed in quotes (single, double, or backticks). Strings are used to represent textual data in programming, such as messages, labels, or inputs.

**Why Are Strings Needed?**  
- To store and display text in applications.  
- To manipulate and process text data, such as user inputs and messages.  
- Strings are foundational for working with textual information in most programming tasks.  

**Example:**  
```javascript
let greeting = "Hello, World!";
console.log(greeting); // Output: Hello, World!
```

---

#### **2. Array Creation and Initialization**

Arrays can be created in several ways. Here are the most common ones:  

**1. Using Square Brackets (Preferred):**  
```javascript
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits); // Output: ["Apple", "Banana", "Cherry"]
```

**2. Using the `Array` Constructor:**  
```javascript
let numbers = new Array(10, 20, 30);
console.log(numbers); // Output: [10, 20, 30]
```

**Importance of Initialization:**  
- Prevents undefined values in the array.  
- Helps maintain consistency and reliability in your program.  

---

#### **3. Accessing and Modifying Array Elements**

Arrays use **indices** to access elements. The first element is at index `0`.

**Accessing Elements:**  
```javascript
let colors = ["Red", "Green", "Blue"];
console.log(colors[1]); // Output: Green
```

**Modifying Elements:**  
```javascript
colors[2] = "Yellow";
console.log(colors); // Output: ["Red", "Green", "Yellow"]
```

**Adding New Elements:**  
```javascript
colors[3] = "Purple";
console.log(colors); // Output: ["Red", "Green", "Yellow", "Purple"]
```

---

#### **4. Common Array Methods**

JavaScript provides several methods for manipulating arrays. Here are four essential ones:  

**1. `push()`**  
Adds an element to the end of the array.  
```javascript
let fruits = ["Apple", "Banana"];
fruits.push("Cherry");
console.log(fruits); // Output: ["Apple", "Banana", "Cherry"]
```

**2. `pop()`**  
Removes the last element from the array.  
```javascript
fruits.pop();
console.log(fruits); // Output: ["Apple", "Banana"]
```

**3. `shift()`**  
Removes the first element of the array.  
```javascript
fruits.shift();
console.log(fruits); // Output: ["Banana"]
```

**4. `unshift()`**  
Adds an element to the beginning of the array.  
```javascript
fruits.unshift("Mango");
console.log(fruits); // Output: ["Mango", "Banana"]
```

---

#### **5. String Manipulation**

Strings are versatile and can be manipulated in various ways.  

**Concatenation:**  
Joining two or more strings together.  
```javascript
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;
console.log(fullName); // Output: John Doe
```

**Slicing:**  
Extracting a portion of a string.  
```javascript
let text = "Hello, World!";
let slicedText = text.slice(0, 5);
console.log(slicedText); // Output: Hello
```

**Substring Extraction:**  
Retrieving a part of a string.  
```javascript
let part = text.substring(7, 12);
console.log(part); // Output: World
```

---

#### **6. Iterating Over Arrays and Strings**

**Iterating Over Arrays:**  
Using a `for` loop to process each element.  
```javascript
let numbers = [10, 20, 30, 40];
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]); // Output: 10, 20, 30, 40
}
```

**Iterating Over Strings:**  
Processing each character of a string.  
```javascript
let word = "JavaScript";
for (let char of word) {
    console.log(char); // Output: J, a, v, a, S, c, r, i, p, t
}
```

---

#### **Combining Arrays and Strings in Daily Life Programming**

Consider a scenario where you need to create a list of items, join them into a string, and display the result:  
```javascript
let items = ["Milk", "Bread", "Eggs"];
let shoppingList = items.join(", ");
console.log(`Shopping List: ${shoppingList}`); 
// Output: Shopping List: Milk, Bread, Eggs
```

---

#### **Problem Statement and Solution**

**Problem:** Write a program to calculate the average of student marks stored in an array and determine if the average marks are greater than a specified threshold.  

**Solution:**  
```javascript
let marks = [85, 90, 78, 88, 92];
let total = 0;

// Calculate the total
for (let i = 0; i < marks.length; i++) {
    total += marks[i];
}

// Calculate the average
let average = total / marks.length;

// Check if the average exceeds the threshold
let threshold = 80;
if (average > threshold) {
    console.log(`Average (${average}) is above the threshold (${threshold}).`);
} else {
    console.log(`Average (${average}) is below the threshold (${threshold}).`);
}

// Output: Average (86.6) is above the threshold (80).
```