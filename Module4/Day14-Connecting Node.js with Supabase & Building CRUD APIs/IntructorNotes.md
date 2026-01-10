

### **Session Name: Connecting Node.js with Supabase & Building CRUD APIs**

## **Learning Objectives**
By the end of this session, students will be able to:

---

## **1. Understand the Need for a Backend Layer over the Database**

- Recall how data was accessed directly via Supabase SQL Editor

- Understand why real-world applications require a backend server

- Identify backend responsibilities such as:

  - Accepting client requests
  - Applying business logic
  - Interacting with the database
  - Sending structured responses

- Understand that the backend acts as a **controlled gateway** to the database

---

## **2. Understand the Role of Node.js and Express in Backend Development**

- Identify **Node.js** as the runtime for backend applications

- Understand Express as a framework that simplifies HTTP handling

- Recall Express concepts already learned:

  - Routes
  - Controllers
  - Request–response cycle

- Understand how Express fits between client and database

---

## **3. Connect a Node.js Backend to Supabase**

- Install and configure the Supabase client in a Node.js project
- Use environment variables to store Supabase credentials securely
- Establish a connection between Express and **Supabase**
- Understand how backend code communicates with the database through the Supabase SDK

---

## **4. Create Database Tables from the Backend (Schema via Backend)**

- Create tables using backend-triggered queries
- Understand when schema changes should be handled via backend vs database console
- Reinforce the idea that backend code can interact with database structure

---

## **5. Build CRUD APIs Using Express and Supabase**

- Create REST APIs for:

  - Creating records
  - Reading records
  - Updating records
  - Deleting records

- Map HTTP methods to CRUD operations

- Understand request flow:

  - Client → Express route → Supabase → Database → Response

---

## **6. Handle Database Responses and Errors in APIs**

- Understand success vs failure responses from Supabase
- Handle errors gracefully in Express controllers
- Send consistent JSON responses to clients
- Understand the importance of proper error handling in backend APIs

---

## **7. Understand the Scope and Limitations of This Integration**

- Clearly understand that:

  - APIs are currently **open**
  - No authentication or authorization is applied yet

- Understand why security is intentionally postponed

- Prepare for backend authentication and authorization in upcoming sessions

---

## **End-of-Session Outcome**

By the end of this session, students will:

- Connect a Node.js backend to a real PostgreSQL database via Supabase
- Build functional CRUD APIs using Express
- Clearly understand backend–database interaction
- Handle database responses and errors correctly
- Be ready to secure APIs using authentication and authorization in the next sessions
