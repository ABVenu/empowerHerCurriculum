[PPT Link](https://docs.google.com/presentation/d/e/2PACX-1vRS0PR2LAqjbLqYpObiz8xFPwOsUv17QKRN3MPFS-A75R7sVcqUb-2fNcyUTWxt01AZfMTIBgQMAoJn/pub?start=true&loop=true&delayms=3000)

### **Student Notes:**
### **Keep Data Specific: Objects & Their Methods**

#### **1. Brief Revision of the Previous Day: Functions**
- **Definition:** A function is a reusable block of code designed to perform a specific task.
- **Why Use Functions?**
  - Avoid repetition of code.
  - Improve modularity and readability.
- **Key Points Recap:**
  - Parameters and arguments.
  - The role of return statements in sending values back from a function.
  - Scope of variables (local vs global).

---

#### **2. Need for Object Data Structure**
- **What Are Objects?**  
  Objects are collections of related data and functionalities stored in key-value pairs.
  - **Example:**
    ```javascript
    let student = {
        name: "John",
        age: 20,
        course: "Mathematics"
    };
    ```
- **Why Use Objects in Programming?**
  - To represent real-world entities (e.g., cars, books, or users).
  - Store multiple related properties in a structured way.
  - Enable organized management of data and behaviors.

---

#### **3. Object Syntax**
- **Creating Objects:**
  - Using **Object Literal Syntax:**
    ```javascript
    let car = {
        brand: "Toyota",
        model: "Corolla",
        year: 2022
    };
    console.log(car.brand); // Toyota
    ```
  - Using **Constructor Function:**
    ```javascript
    let car = new Object();
    car.brand = "Tesla";
    car.model = "Model X";
    car.year = 2023;
    console.log(car); // { brand: "Tesla", model: "Model X", year: 2023 }
    ```

---

#### **4. Accessing Object Properties**
- **Dot Notation:**  
  Used to access properties with fixed names.  
  ```javascript
  console.log(car.brand); // Toyota
  ```
- **Bracket Notation:**  
  Used to access properties with dynamic names or special characters.  
  ```javascript
  let property = "model";
  console.log(car[property]); // Corolla
  ```
- **When to Use Which?**
  - Dot notation is simpler and more readable.
  - Bracket notation is useful for dynamic or invalid property names.

---

#### **5. Traversing an Object**
- Use the `for...in` loop to iterate over object properties:  
  ```javascript
  let car = { brand: "Toyota", model: "Corolla", year: 2022 };

  for (let key in car) {
      console.log(`${key}: ${car[key]}`);
  }
  // Output:
  // brand: Toyota
  // model: Corolla
  // year: 2022
  ```


---

#### **6. Object Methods**
- **What Are Methods?**  
  Functions stored as object properties are called methods.  
  - Methods allow objects to perform specific tasks or calculations.  
  - **Example:**
    ```javascript
    let rectangle = {
        length: 5,
        width: 3,
        area: function() {
            return this.length * this.width;
        }
    };
    console.log(rectangle.area()); // 15
    ```

---

#### **7. Introduction to the `this` Keyword**
- **What Is `this`?**  
  - In an object method, `this` refers to the object that calls the method.
  - It allows access to other properties and methods within the same object.
  - **Example:**
    ```javascript
    let person = {
        name: "Alice",
        greet: function() {
            return `Hello, my name is ${this.name}.`;
        }
    };
    console.log(person.greet()); // Hello, my name is Alice.
    ```
- **Important Notes:**
  - In methods, `this` refers to the object that owns the method.
  - Outside of methods, `this` behaves differently depending on the environment.

---

#### **Summary Table: Object Syntax and Operations**

| **Operation**           | **Syntax**                               | **Example**                                                   |
|--------------------------|-------------------------------------------|---------------------------------------------------------------|
| Creating Object          | `let obj = { key: value };`              | `let car = { brand: "Toyota", model: "Corolla" };`            |
| Accessing Properties     | Dot: `obj.key` <br> Bracket: `obj[key]`  | `car.brand // Toyota` <br> `car["model"] // Corolla`          |
| Adding Property          | `obj.newKey = value;`                    | `car.year = 2022;`                                            |
| Updating Property        | `obj.key = newValue;`                    | `car.model = "Camry";`                                        |
| Deleting Property        | `delete obj.key;`                        | `delete car.year;`                                            |
| Traversing Properties    | `for (let key in obj)`                   | `for (let key in car) { console.log(key); }`                  |
| Adding Methods           | `obj.method = function() { };`           | `car.drive = function() { return "Vroom"; };`                 |
| Calling Methods          | `obj.method()`                           | `car.drive();`                                                |

---

#### **Practice Problem:**
**Problem Statement:**  
Create an object called `book` to represent a book in a library with the following properties and methods:
- `title` (string): Name of the book.
- `author` (string): Author's name.
- `pages` (number): Total number of pages.
- Method: `describe()` that returns a string with all book details.

**Solution:**  
```javascript
let book = {
    title: "JavaScript Essentials",
    author: "Jane Doe",
    pages: 300,
    describe: function() {
        return `The book "${this.title}" by ${this.author} has ${this.pages} pages.`;
    }
};

console.log(book.describe());
// Output: The book "JavaScript Essentials" by Jane Doe has 300 pages.
```

---