## **Learning Objectives – Standard Project-Coding Structure & Database Fundamentals**

By the end of this session, students will be able to:

---

## **1. Understand the Need for a Standard Backend Project Structure**

* Explain why unstructured code becomes difficult to:

  * Maintain
  * Debug
  * Scale
* Understand how real-world backend projects are organized
* Recognize the importance of separation of concerns in backend applications

---

## **2. Understand MVC-Based Code Segregation**

* Explain the purpose of segregating code into:

  * **Models** – data structure and database interaction
  * **Controllers** – business logic and request handling
  * **Routes** – request-to-controller mapping
* Understand how MVC improves:

  * Readability
  * Testability
  * Team collaboration
* Identify how routing, controllers, and models interact in a request lifecycle

---

## **3. Organize an Express Project Using a Standard Folder Structure**

* Identify commonly used folders and files:

  * `routes/`
  * `controllers/`
  * `models/`
  * `config/`
  * `middlewares/`
  * `index.js` / `app.js`
* Understand the responsibility of each folder
* Explain how this structure supports scalable backend development

---

## **4. Understand Environment Variables and `.env` File Usage**

* Define **environment variables** and their purpose
* Explain why sensitive data should never be hardcoded
* Store configuration values such as:

  * Port numbers
  * Database credentials
  * API keys
* Understand how `.env` files differ across environments:

  * Development
  * Testing
  * Production

---

## **5. Understand Error Handling and `try-catch` in Backend Code**

* Explain why backend systems must handle runtime failures gracefully
* Use `try-catch` blocks to handle:

  * Database errors
  * Runtime exceptions
  * Unexpected failures
* Understand how proper error handling improves:

  * Application stability
  * Debugging experience
  * User-facing error responses

---

## **6. Understand Why `db.json` Is Not Suitable for Real Applications**

* Identify limitations of file-based storage like `db.json`:

  * Slow read/write operations
  * No concurrency control
  * High risk of data corruption
  * Poor scalability
* Understand why real applications require dedicated databases
* Recognize file-based storage as suitable only for learning or prototyping

---

## **7. Understand Ideal Characteristics of a Database System**

* Identify key characteristics of a production-ready database:

  * **Fast** – optimized for high-performance queries
  * **Efficient** – handles large volumes of data
  * **Safe** – ensures data integrity and consistency
  * **Reliable** – prevents data loss
  * **Concurrent** – supports multiple users simultaneously
  * **Globally available** – supports distributed access and scaling
* Understand why databases are central to backend systems

---

## **8. Understand Types of Databases**

* Classify databases into:

  * **Relational Databases**
  * **Non-Relational (NoSQL) Databases**
* Understand how data is stored differently in each type
* Identify scenarios where each type is appropriate

---

## **9. Understand Relational Databases**

* Define relational databases as:

  * Table-based
  * Schema-driven
  * Structured using rows and columns
* Understand concepts such as:

  * Tables
  * Rows and columns
  * Primary keys and relationships
* Identify common use cases:

  * Financial systems
  * Enterprise applications
  * Data consistency–critical systems

---

## **10. Understand Non-Relational (NoSQL) Databases**

* Define NoSQL databases as:

  * Schema-less or flexible-schema
  * Designed for horizontal scaling
* Identify common types:

  * Document-based
  * Key–value stores
* Understand use cases such as:

  * High-traffic applications
  * Rapidly changing data models
  * Real-time systems

---

## **11. Compare Relational vs Non-Relational Databases**

* Clearly differentiate based on:

  * Structure
  * Schema enforcement
  * Scalability
  * Query complexity
  * Data consistency
* Choose the appropriate database type based on application needs
* Understand trade-offs involved in database selection

---

## **12. Understand the Database Used in This Course**

* Identify **PostgreSQL** as the database used in this course
* Understand why PostgreSQL is chosen:

  * Strong relational capabilities
  * Advanced querying support
  * High reliability and data integrity
  * Widely used in industry
* Prepare to learn:

  * Database fundamentals
  * SQL queries
  * Integration with Node.js and Express

---

## **End-of-Session Outcome**

By the end of this session, students will:

* Organize backend projects using industry-standard structure
* Write cleaner, maintainable Express applications
* Understand why real databases are required in backend systems
* Clearly differentiate between database types
* Be conceptually prepared to start working with PostgreSQL


