## **Learning Objectives – Express.js Middleware**


## **1. Understand What Middleware Is in Express.js**

* Define **middleware** as functions that:

  * Have access to the request and response objects
  * Execute during the request–response lifecycle
* Explain where middleware fits between:

  * Client request
  * Route handler
* Recognize **Express.js** as a framework that relies heavily on middleware for extensibility

---

## **2. Understand the Middleware Execution Flow**

* Understand the **middleware chain** concept
* Explain the role of the `next()` function
* Identify how control moves from one middleware to the next
* Understand what happens when `next()` is not called

---

## **3. Identify Types of Middleware in Express**

* Classify middleware into:

  * Built-in middleware
  * Custom middleware
  * External (third-party) middleware
* Understand when and why each type is used

---

## **4. Understand Built-in Middleware in Express**

* Identify commonly used built-in middleware:

  * `express.json()` – parse JSON request bodies
  * `express.urlencoded()` – parse URL-encoded form data
  * `express.static()` – serve static files
* Explain real-world use cases for each built-in middleware
* Understand how built-in middleware simplifies request processing

---

## **5. Create and Use Custom Middleware**

* Define **custom middleware** as user-defined functions
* Create middleware for:

  * Logging requests
  * Validating input
  * Authentication checks (introductory)
* Understand how to:

  * Access `req`, `res`, and `next`
  * Modify request objects
  * Control request flow

---

## **6. Use External (Third-Party) Middleware**

* Define **external middleware** as packages installed via NPM
* Identify commonly used external middleware such as:

  * `morgan` – request logging
  * `cors` – Cross-Origin Resource Sharing
* Understand how external middleware integrates into Express applications
* Explain why external middleware improves development speed and reliability

---

## **7. Understand Middleware Levels (Layers) in an Express Application**

* Explain middleware placement and scope:

  * **Application-level middleware**
  * **Router-level middleware**
  * **Route-level middleware**
* Understand how middleware execution differs at each level
* Choose the appropriate middleware level based on use case

---

## **8. Apply Application-Level Middleware**

* Use `app.use()` to apply middleware globally
* Understand use cases such as:

  * Request parsing
  * Global logging
  * Security headers
* Explain how order of middleware affects execution

---

## **9. Apply Router-Level Middleware**

* Attach middleware to `express.Router()`
* Apply middleware to:

  * All routes in a router
  * Selected router paths
* Understand router isolation and modularity

---

## **10. Apply Route-Level Middleware**

* Attach middleware to individual routes
* Control access to specific endpoints
* Chain multiple middleware functions in a single route

---

## **11. Handle Undefined Routes (404 – Not Found)**

* Define **undefined routes** as requests that do not match any route
* Create a fallback middleware for handling 404 errors
* Understand why the 404 handler must be placed at the end
* Send meaningful 404 responses to clients

---

## **12. Understand Error-Handling Middleware (Conceptual Introduction)**

* Recognize error-handling middleware by its four parameters:

  * `err, req, res, next`
* Understand how Express differentiates normal middleware from error middleware
* Prepare for advanced error handling in future sessions

---

