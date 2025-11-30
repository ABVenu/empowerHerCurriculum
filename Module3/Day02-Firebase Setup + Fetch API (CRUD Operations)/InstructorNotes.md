### Lecture Name

### **Firebase Setup + Fetch API (CRUD Operations)**

### Learning Objectives

By the end of this session, students will be able to:

- Define Firebase and explain its role as a Backend-as-a-Service (BaaS).
- Configure and connect a Firebase Realtime Database.
- Understand REST API endpoints used with Firebase.
- Perform CRUD operations (Create, Read, Update, Delete) using Fetch API.
- Handle JSON responses from APIs and display data dynamically using the DOM.
- Apply best practices in network-based communication between frontend and backend.

---

## 1. Introduction to Firebase

### What is Firebase?

Firebase is a Backend-as-a-Service (BaaS) platform by Google that provides cloud-based services such as:

- Realtime Database (focus of this session)
- Authentication
- Hosting
- Cloud Functions
- Storage and Analytics

Firebase Realtime Database:

- A NoSQL database
- Stores data in JSON format
- Supports real-time synchronization across clients

---

## 2. Firebase Realtime Database Setup

### Step 1: Create Firebase Project

1. Open Firebase Console.
2. Select **Add Project**.
3. Enter a project name (example: `my-demo-app`).
4. Disable Analytics (optional for learning).
5. Create the project.

### Step 2: Enable Realtime Database

Inside Firebase:

1. Navigate to **Build → Realtime Database**.
2. Select **Create Database**.
3. Choose a location (Asia-South recommended for India region).
4. Select **Start in Test Mode**.

This automatically sets rules to allow read/write operations without authentication.

### Default Test Mode Rules

```json
{
  "rules": {
    ".read": "true",
    ".write": "true"
  }
}
```

> Note: Test mode is only for learning and should not be used in production.

### Step 3: Copy Database URL

Example database URL:

```
https://my-demo-app-default-rtdb.firebaseio.com/
```

All Firebase REST API requests must end with `.json`

---

## 3. Firebase REST API Endpoint Format

Collection Example: `students`

Endpoint:

```
https://my-demo-app-default-rtdb.firebaseio.com/students.json
```

Record with ID Example:

```
https://my-demo-app-default-rtdb.firebaseio.com/students/<id>.json
```

---

## 4. CRUD Operations using Fetch API

CRUD stands for:
Create | Read | Update | Delete

Each action maps to an HTTP method.

---

### 4.1 Create (POST Request)

```js
fetch("https://my-demo-app-default-rtdb.firebaseio.com/students.json", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    name: "Rahul",
    age: 20,
  }),
})
  .then((res) => res.json())
  .then((data) => console.log("POST Response:", data));
```

- Firebase generates a unique ID automatically.

---

### 4.2 Read (GET Request)

```js
fetch("https://my-demo-app-default-rtdb.firebaseio.com/students.json")
  .then((res) => res.json())
  .then((data) => console.log("GET Data:", data));
```

- Returns all student records from database.

---

### 4.3 Update Full Record (PUT)

Requires the unique record ID:

Example ID: `-NuVSxxYspT1asA7Hd9w`

```js
fetch(
  "https://my-demo-app-default-rtdb.firebaseio.com/students/-NuVSxxYspT1asA7Hd9w.json",
  {
    method: "PUT",
    headers: {
      "Content-Type": "application/json",
    },
    body: JSON.stringify({
      name: "Rahul",
      age: 21,
      course: "React",
    }),
  }
)
  .then((res) => res.json())
  .then((data) => console.log("PUT Response:", data));
```

---

### 4.4 Partial Update (PATCH)

```js
fetch(
  "https://my-demo-app-default-rtdb.firebaseio.com/students/-NuVSxxYspT1asA7Hd9w.json",
  {
    method: "PATCH",
    body: JSON.stringify({
      age: 22,
    }),
  }
)
  .then((res) => res.json())
  .then((data) => console.log("PATCH Response:", data));
```

---

### 4.5 Delete (DELETE)

```js
fetch(
  "https://my-demo-app-default-rtdb.firebaseio.com/students/-NuVSxxYspT1asA7Hd9w.json",
  {
    method: "DELETE",
  }
).then(() => console.log("Record Deleted"));
```

---

## 5. CRUD Operation Mapping Table

| Operation             | HTTP Method | Endpoint              | Description             |
| --------------------- | ----------- | --------------------- | ----------------------- |
| Create                | POST        | `/students.json`      | Adds new record         |
| Read                  | GET         | `/students.json`      | Fetches all records     |
| Replace Entire Record | PUT         | `/students/<id>.json` | Updates full object     |
| Partial Update        | PATCH       | `/students/<id>.json` | Updates selected fields |
| Delete                | DELETE      | `/students/<id>.json` | Removes record          |

---

## 6. Practical Task

Students must:

1. Add a student record via POST
2. Fetch and display all students on the UI
3. Attach Update and Delete buttons to each record
4. Apply PUT or PATCH and DELETE operations from the UI

---

## 7. Key Takeaways

- Firebase provides backend features without a server.
- Fetch API is used to communicate with Firebase via HTTP methods.
- Realtime Database uses JSON-based NoSQL structure.
- CRUD operations allow complete interaction with stored data.

---
