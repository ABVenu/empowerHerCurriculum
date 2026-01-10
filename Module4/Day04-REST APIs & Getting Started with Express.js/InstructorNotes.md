## **Learning Objectives**

By the end of this session, students will be able to:

---

## **1. Reposition Node.js as a Backend System**

- Understand that Node.js is not meant only for exploring built-in modules
- Explain Node.js as a platform to:

  - Build backend systems
  - Accept requests from frontend applications
  - Process business logic
  - Send responses

- Relate backend systems to React frontend applications making HTTP requests

---

## **2. Understand Frontend–Backend Communication Flow**

- Explain how frontend applications communicate with backend systems
- Identify frontend responsibilities:

  - Triggering requests
  - Handling responses

- Identify backend responsibilities:

  - Accepting requests
  - Processing logic
  - Sending structured responses

---

## **3. Understand the Request–Response Cycle**

- Define the request–response cycle
- Identify components of a request:

  - HTTP method
  - Endpoint (URL path)

- Identify components of a response:

  - Response body
  - HTTP status code

- Understand that each request receives exactly one response

---

## **4. Understand APIs and REST Fundamentals**

- Define an API as a communication interface between systems
- Define REST API and explain:

  - Statelessness
  - Resource-based design

- Compare REST with other API styles at a high level
- Understand why REST APIs are widely used in modern web applications
- Recognize REST API adoption by large-scale industry systems

---

## **5. Understand REST API Building Blocks**

- Identify HTTP methods (introductory overview):

  - GET
  - POST
  - PUT / PATCH
  - DELETE

- Understand request body vs response body (conceptual)
- Understand HTTP status codes and their role in communication
- Identify JSON as the standard response format for frontend consumption

---

## **6. Understand Why Express.js Is Required**

- Identify limitations of handling HTTP manually using Node.js
- Understand Express.js as:

  - A minimal framework built on Node.js
  - A tool that simplifies request handling

- Recognize Express as an external module installed using NPM

---

## **7. Setup a Basic Express Application**

- Import Express and create an application instance
- Start an HTTP server listening on a specific port
- Understand what it means for a backend server to be “running”

---

## **8. Understand a Typical GET Request in Express**

### **Code Example**

```js
app.get("/home", (req, res) => {
  res.json({ message: "Welcome to Home Page" });
});
```

### **Conceptual Breakdown**

Students will be able to:

- Explain what `.get()` means:

  - `.get()` is used to handle **HTTP GET requests**
  - GET requests are meant to **retrieve data**

- Explain what `"/home"` represents:

  - It is an **endpoint (route)**
  - It represents a specific resource or path

- Explain the callback function:

  - It runs **when a request hits this route**
  - It receives:

    - `req` → request object (data sent by client)
    - `res` → response object (used to send response)

- Understand that Express internally:

  - Listens for requests
  - Matches route + method
  - Executes the callback

---

## **9. Explore Multiple GET Requests**

- Create and understand multiple GET endpoints such as:

  ```js
  app.get("/", (req, res) => {
    res.send("Server is running");
  });

  app.get("/about", (req, res) => {
    res.send("<h1>About Page</h1>");
  });

  app.get("/api/status", (req, res) => {
    res.json({ status: "OK", uptime: "running" });
  });
  ```

- Understand how different routes serve different responses
- Observe route matching behavior

---

## **10. Demonstrate GET Requests Using the Browser**

- Use the browser to access GET endpoints:

  - `http://localhost:3000/`
  - `http://localhost:3000/home`
  - `http://localhost:3000/about`

- Understand why browser is suitable for GET requests:

  - Browser sends GET requests by default

- Observe:

  - Text responses
  - HTML rendering
  - JSON output

- Use browser as a simple API testing tool

---

## **11. Understand the Response Object (`res`)**

- Identify `res` as the object used to send data back to the client
- Use different response methods:

  - `res.send()` for text or HTML
  - `res.json()` for structured data

- Understand how Express automatically sets headers

---

## **12. Decide Between `res.send()` and `res.json()`**

- Understand that:

  - `res.send()` is flexible and supports multiple formats
  - `res.json()` is specific to JSON responses

- Fix `res.json()` as the standard for REST APIs
- Justify the decision based on:

  - REST conventions
  - React frontend expectations
  - Consistent API design

---

## **13. Relate GET APIs to Real-World Use Cases**

- Map GET APIs to use cases such as:

  - Fetching homepage data
  - Checking server health
  - Fetching user profiles

- Understand that frontend applications consume these APIs

---

## **14. Prepare for POST Requests and Data Handling**

- Understand that GET requests:

  - Fetch data
  - Do not modify server state

- Build readiness for:

  - POST requests
  - Request body handling
  - Middleware usage

- Prepare for real-world flows like:

  - Signup
  - Login
  - Form submission

---

## **End-of-Session Outcome**

By the end of Day 4, students will:

- Clearly explain REST APIs and request–response cycle
- Understand Express routing fundamentals
- Explain every part of a GET request in Express
- Create and test GET APIs using the browser
- Send consistent JSON responses
- Be ready to handle POST requests and real data in the next session

---
