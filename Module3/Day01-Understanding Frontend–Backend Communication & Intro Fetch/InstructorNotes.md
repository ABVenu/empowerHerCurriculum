### Lecture Name

### **Understanding Frontend–Backend Communication & Intro Fetch**

### Learning Objectives

By the end of this session, students will be able to:

### **A. Frontend & Backend Communication**

1. **Explain the role of the Frontend**

   - Identify how UI displays and collects data from users.
   - Understand that frontend does not manage data storage or business logic.

2. **Describe what the Backend does**

   - Explain how backend processes data, handles business rules, secures data, and manages databases.

3. **Understand Business Logic**

   - Define business logic and provide real-world examples of how backend controls decisions.

4. **Define what a Database is**

   - Differentiate between relational and non-relational databases.
   - Explain why backend applications need databases for persistent data.

5. **Describe the Client–Server Model**

   - Understand the roles of client (browser) and server (backend) in communication.

6. **Explain the Request–Response Cycle**

   - Identify HTTP request types: GET, POST, PUT, DELETE.
   - Explain status codes and when they are used (like 200, 404).

---

### **B. Fetch API & Asynchronous Operations**

7. **Use the Fetch API** to communicate with backend APIs

   - Perform GET requests using fetch
   - Understand how to handle asynchronous server responses

8. **Explain Promises and Asynchronous Behavior**

   - Understand why fetch is asynchronous
   - Describe what `.then()`, `.catch()` do and why two `.then()` are needed

9. **Use async / await syntax**

   - Convert fetch requests from `.then()` style to `async/await`
   - Explain why two `await`s are needed (fetch + JSON conversion)

10. **Display fetched data in UI**

- Retrieve JSON data and render it dynamically using DOM manipulation

---

### Detailed Notes

### **Part A: Understanding Frontend Backend Communication**

#### **1. Understanding Frontend Development**

- It is the visible part of a web application that users interact with (UI).
- It displays data received from the backend and collects inputs from users.
- Its main goal is to provide a smooth **user experience** by updating the interface based on data.
- Frontend is not responsible for data management/storage and bussiness logic

#### **2. Understanding Backend Development**

- **What is Backend Development?**
  - Backend development refers to the server-side development of a web application, where the application’s data is processed, stored, and managed.
  - It involves creating logic for handling user requests, interacting with databases, and serving the appropriate responses.
- **Typical Tasks Handled by Backend Developers:**
  - Managing databases (CRUD operations).
  - Ensuring security (authentication, authorization).
  - Developing APIs (Application Programming Interfaces).
  - Business logic implementation (processing data, transactions).
- **Common Backend Languages and Frameworks:**
  - Python (with frameworks like Django, Flask)
  - Node.js (with Express.js)
  - Java (with Spring Boot)

---

#### **3. Business Logic**

- **What is Business Logic?**
  - Business logic refers to the rules or operations that drive the functionality of the application.
  - It's the code that defines how data is created, stored, and changed in accordance with business rules.
- **Examples of Business Logic:**
  - Applying discounts in an e-commerce application, Here Backend takes decision whether to apply discount or no, Frontend simply displays discounted price
  - Return policy of E-commerce website, how many days returns policy is decided by backend, FE simply displays returns available or not available

---

#### **4. What are Databases?**

- **Definition and Importance:**
  - Databases store, retrieve, and manage data for backend applications. They are crucial for applications that require persistent data storage (e.g., user information, product listings).
- **Types of Databases:**

  - **Relational Databases (e.g., MySQL, PostgreSQL):**

    - Structured data, uses tables with rows and columns.
    - Data is stored in a specific format, typically requiring a predefined schema.

  - **Non-relational Databases (e.g., MongoDB, Firebase):**
    - Flexible, schema-less data storage.
    - Suitable for unstructured data (e.g., JSON, key-value pairs).

- **Use Cases:**
  - Relational: Suitable for structured data where relationships between data entities are important (e.g., banking systems).
  - Non-relational: Ideal for applications with unstructured or rapidly changing data (e.g., social media, IoT devices).

> Please Note, you will learn Backend Development - Databases in next module, now just understand what BE does?, what DB does?, just the mechanism that's all

---

#### **5. Connecting Backend to Databases**

- **How Backend Applications Query Databases:**
  - Databases interact with backend applications via queries. These can be simple or complex depending on the data needs.

---

#### **6. Client-Server Model**

- **What is the Client-Server Model?**
  - In the client-server model, the client (typically a web browser or app) makes requests to the server (backend), and the server processes those requests and sends back data.
- **Real-World Analogy:**
  - Client: The customer who orders food.
  - Server: The chef who prepares and delivers the food.

---

#### **7. Request-Response Cycle**

The Client–Server Model works based on a **Request–Response Cycle**.
The **client (frontend)** always makes a request, and the **server (backend)** always sends a response.

- **Request:**
  The frontend sends a request to the backend using HTTP methods such as GET, POST, PUT, and DELETE.
  This request can include any data the server needs to process, such as form inputs.

- **Response:**
  After processing the request, the backend sends a response back to the frontend.
  The response contains a status code (like 200 for success or 404 for not found) and data (often JSON or HTML) that the frontend will display to the user.

**Example:**

- When you open an LMS and type your email and password, then click the Login button
  - — the frontend sends your login details to the backend.
- The backend checks whether the credentials are correct.
  - If they are valid, the backend responds by showing the dashboard page. If the credentials are wrong, the backend responds with a message saying the password is incorrect.
- This entire process — sending data to the server and receiving the result — is the Request-Response Cycle.

- **HTTP Methods in Request-Response Cycle:**

  - **GET:** Ask for data from the server.
  - **POST:** Send new data to the server.
  - **PUT:** Update existing data in the server.
  - **DELETE:** Remove data from the server.

---

### **Part B: Fetch**

Now that we understand how the Frontend and Backend communicate using HTTP methods, we need a way for the Frontend to actually send these requests to the Backend. This communication happens through APIs, and in JavaScript, the function used to call these APIs is called **fetch**.

The **fetch** function allows the Frontend to:
• get data from the Backend
• send new data to the Backend
• update existing data
• delete data

These actions are mapped to HTTP methods:
• **GET** → Get or Read data from the server
• **POST** → Send new data to the server
• **PUT / PATCH** → Update existing data on the server
• **DELETE** → Remove data from the server

Fetch is not an instant action. It involves:

1. Contacting the server
2. Waiting for the server to process the request
3. Receiving the response back

Since this takes time, **fetch is an asynchronous task**. It does not stop the entire program while waiting for the server. Instead, fetch returns a **Promise**, which tells JavaScript:
“Continue the program… I will give you the result when I get it.”

To know whether fetch succeeded or failed, we must handle the Promise.
This is where `.then()` and `.catch()` come into use or alternatively `async` and `await`.

> This is one of the real-life uses of Promises in JavaScript.

### **Syntax of fetch**

```js
fetch("API_URL", {
  method: "HTTP_METHOD",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data), // Only for POST/PUT/PATCH
})
  .then((response) => response.json())
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log("Error:", error);
  });
```

---

### Example method usage:

- GET → only URL needed
- POST/PUT/PATCH/DELETE → URL + method + data

---

### Fetch GET Request — Two Approaches

We are making a GET request to:
`https://jsonplaceholder.typicode.com/todos`

We will use two separate functions:

1. Fetch/get the data
2. Append the data into UI

---

## Approach 1: Using `.then()`

```js
// Function 1: Get Data from API
function getTodos() {
  fetch("https://jsonplaceholder.typicode.com/todos")
    .then((response) => response.json()) // Step 1: Convert response to JSON
    .then((data) => {
      // Step 2: Now we can use JSON data
      appendTodos(data);
    })
    .catch((error) => {
      console.log("Error fetching data:", error);
    });
}

// Function 2: Append Data to UI
function appendTodos(todos) {
  const list = document.getElementById("todoList");

  todos.forEach((item) => {
    const li = document.createElement("li");
    li.textContent = item.title;
    list.appendChild(li);
  });
}

getTodos();
```

---

## Why `.then()` is used Two Times?

1. **First `.then()`**
   Receives the server response (not readable yet)
   Converts it into JSON using `response.json()`

2. **Second `.then()`**
   Receives the actual usable JSON data
   We can now display it in UI

This is done because converting response into JSON is also an asynchronous process.

---

## Approach 2: Using `async / await`

```js
// Function 1: Get Data from API
async function getTodos() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/todos");
    const data = await response.json(); // Convert to JSON
    appendTodos(data);
  } catch (error) {
    console.log("Error fetching data:", error);
  }
}

// Function 2: Append Data to UI
function appendTodos(todos) {
  const list = document.getElementById("todoList");

  todos.forEach((item) => {
    const li = document.createElement("li");
    li.textContent = item.title;
    list.appendChild(li);
  });
}

getTodos();
```

---

## Why two `await`?

1. `await fetch(...)`
   Waits for the server to respond

2. `await response.json()`
   Waits for converting data into JSON format

Both steps take time, so both must be awaited.

---

### HTML for UI Rendering

```html
<ul id="todoList"></ul>
```

---

- The remaining methods like POST, PUT, and DELETE will be practiced in the next session once we set up our own dummy backend — Firebase. There, students will send real data, update it, and delete it from their own database using fetch.
