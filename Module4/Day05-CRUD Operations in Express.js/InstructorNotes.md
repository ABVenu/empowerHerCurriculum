## **Learning Objectives**

By the end of this session, students will be able to:

---

## **1. Quick Recap & Project Reinitialization**

- Recall key concepts from Day 4:

  - REST APIs
  - Express server setup
  - GET requests
  - Request–response cycle

- Start a **new Express project** with:

  - Basic folder structure
  - Express setup
  - Server listening on a port

- Create and test basic GET routes:

  - `/home`
  - `/aboutus`

- Reinforce confidence in setting up a backend project from scratch

---

## **2. Understand the Need for Automatic Server Restart**

- Observe the problem:

  - Server must be manually restarted after every code change

- Understand why this slows down backend development
- Identify the need for a tool that:

  - Watches file changes
  - Automatically restarts the server

---

## **3. Introduce Nodemon**

- Define **nodemon** as a development utility for Node.js
- Explain how nodemon:

  - Monitors file changes
  - Automatically restarts the server

- Understand why nodemon is used **only in development**
- Run the server using nodemon instead of `node`
- Observe live reload behavior after code changes

---

## **4. Introduce HTTP Methods Beyond GET**

- Recall that:

  - GET is used to fetch data

- Understand that backend systems must also:

  - Accept data
  - Modify data
  - Remove data

- Introduce other HTTP methods conceptually:

  - POST
  - PUT / PATCH
  - DELETE

---

## **5. Understand and Create the First POST Request**

- Understand POST as a method used to **send data to the backend**
- Create a simple POST route in Express:

  - Endpoint example: `/first-post`

- Send a response such as:

  - `"This is first POST request"`

- Understand that POST routes are **not accessible directly from the browser**

---

## **6. Understand the Need for API Testing Tools**

- Identify the limitation of browsers:

  - Browsers can easily test only GET requests

- Understand why backend developers need specialized tools to:

  - Send POST, PUT, DELETE requests
  - Attach request bodies
  - Inspect responses clearly

---

## **7. Introduce Postman**

- Define **Postman** as an API testing tool
- Explain why Postman is essential for backend developers:

  - Testing all HTTP methods
  - Sending request bodies
  - Viewing structured responses

- Understand Postman as a **client** that communicates with backend APIs
- Use Postman to:

  - Send a POST request
  - Observe server response

---

## **8. Understand Data Persistence Using a File**

- Introduce a simple data storage approach using a `db.json` file
- Understand that:

  - This file acts as a temporary database
  - Data persists across server restarts

- Store and manage todos inside `db.json`
- Use `fs` modules of Node JS to make CRUD operations of `db.json`.

---

## **9. Implement GET Operation for Todos**

- Create a GET API to:

  - Read todos from `db.json`
  - Send todos as a JSON response

- Understand file reading flow:

  - Read file
  - Parse JSON
  - Send response

- Test the GET todos API using Postman and browser

---

## **10. Implement CREATE (POST) Operation for Todos**

- Create a POST API to:

  - Add a new todo
  - Accept todo data from request body

- Understand the need to:

  - Read incoming request body
  - Append new todo to existing data
  - Save updated data back to `db.json`

- Send meaningful success response after creation

---

## **11. Understand `express.json()`**

- Understand the purpose of `express.json()`:

  - To read and parse incoming JSON data

- Activate JSON parsing at application start
- Understand that without it:

  - POST request body cannot be accessed

- Reinforce this as a **mandatory setup step for REST APIs**

---

## **12. Implement UPDATE Operation for Todos**

- Create an API to update a todo:

  - Todo ID sent through request body

- Understand update flow:

  - Find todo by ID
  - Modify its values
  - Save updated list back to `db.json`

- Send appropriate response:

  - Update success
  - Todo not found

---

## **13. Implement DELETE Operation for Todos**

- Create an API to delete a todo by ID
- Understand delete flow:

  - Read existing todos
  - Remove matching todo
  - Save updated data

- Send confirmation response after deletion

---

## **14. Test Complete CRUD Flow Using Postman**

- Use Postman to test:

  - GET all todos
  - POST new todo
  - UPDATE existing todo
  - DELETE todo

- Observe:

  - Request body
  - Response body
  - Status codes (basic understanding)

---

## **15. Relate CRUD APIs to Real Applications**

- Map todo CRUD APIs to real-world scenarios:

  - Task management systems
  - Notes apps
  - Backend services for React apps

- Understand how frontend applications will later:

  - Consume these APIs
  - Render data dynamically

---

## **End-of-Session Outcome**

By the end of Day 5, students will:

- Confidently use nodemon for development
- Understand and use POST requests
- Test APIs using Postman
- Build complete CRUD APIs using Express
- Persist data using a file-based approach
- Be ready to integrate backend APIs with frontend applications

---
