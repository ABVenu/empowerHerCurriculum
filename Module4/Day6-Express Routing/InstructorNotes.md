# **🕒 Hour 1: Core Express Routing Concepts**

---

## **1. Understand What a Route Is in Express.js**

- Define a **route** as the combination of:

  - HTTP method
  - Endpoint (URL path)
  - Route handler function

- Explain how routes map client requests to backend logic
- Recognize **Express.js** as a framework that simplifies request handling and routing

---

## **2. Understand Endpoints and URL Design**

- Define an **endpoint** as a unique URL path
- Differentiate between:

  - Static endpoints
  - Dynamic endpoints

- Follow RESTful naming conventions for endpoints
- Understand how endpoint design impacts API readability

---

## **3. Understand Dynamic Routing Using Path Parameters**

- Define **path parameters** as dynamic URL segments
- Identify path parameters using the `:` syntax
- Access dynamic values using `req.params`
- Explain real-world use cases such as:

  - Fetching data by ID
  - Updating a specific resource

- Demonstrate by example code

---

## **4. Understand Query Parameters**

- Define **query parameters** as optional URL modifiers
- Identify query parameters using `?` and `&`
- Access query parameters using `req.query`
- Explain use cases:

  - Filtering
  - Sorting
  - Pagination
  - Searching

---

## **5. Differentiate Between Path Parameters and Query Parameters**

- Clearly distinguish:

  - Path parameters → identify a resource
  - Query parameters → refine or modify results

- Apply best practices for RESTful API design
- Demonstrate by example code

---

## **6. Handle Multiple Routes in an Express Application**

- Understand route matching order in Express
- Organize routes to avoid conflicts
- Group routes logically based on features or resources

---

# Express Router (Modular Routing)\*\*

---

## **7. Understand the Need for Express Router**

- Identify problems with monolithic `app.js` routing
- Understand scalability and maintainability challenges
- Recognize when to move from basic routing to modular routing

---

## **8. Use Express Router for Modular Routing**

- Explain the purpose of `express.Router()`
- Create router-level routes for a specific resource
- Mount routers using `app.use()` with a base path
- Understand how router paths combine with base paths

---

## 9. Organise previosuly created CRUD into Routes using Express.Router()

---

## **End-of-Session Outcome**

By the end of this 2-hour session, students will:

- Clearly explain every part of an Express route
- Design clean and RESTful endpoints
- Use path and query parameters effectively
- Build modular and scalable routing using Express Router

---
