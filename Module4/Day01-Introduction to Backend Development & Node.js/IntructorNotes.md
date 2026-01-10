## **Learning Objectives**

By the end of this session, students will be able to:

---

### **1. Recall the Current Frontend-Only Architecture**

- Identify how applications built so far (React + Firebase) operate primarily as **frontend-driven systems**
- Recognize that frontend responsibilities mainly focus on:

  - User Interface (UI)
  - User Experience (UX)
  - Input collection and validation

- Explain the **limitations of frontend-only logic** in real-world applications

---

### **2. Distinguish Between UI Logic and Business Logic**

- Define **business logic** and explain why it must not reside in the frontend
- Analyze real-world examples of business logic such as:

  - Discount calculation in e-commerce systems
  - Password reset attempt limits
  - Authorization rules and access control

- Justify why:

  - Business rules must be **centralized**
  - Data consistency must be **enforced at the backend**
  - Frontend should only consume outcomes, not decide rules

---

### **3. Understand What Backend Is and Why It Is Needed**

- Define **backend** as a system responsible for:

  - Business logic execution
  - Data processing and validation
  - Secure interaction with databases

- Explain how backend acts as a **single source of truth** for the application
- Compare frontend and backend responsibilities in a full-stack system

---

### **4. Explain Where Frontend and Backend Run**

- Describe where frontend applications run:

  - Inside the **browser**
  - Dependent on browser-provided capabilities

- Describe where backend applications run:

  - On a **server**
  - Independent of the browser

- Differentiate between:

  - Browser environment
  - Server environment

---

### **5. Understand the Client–Server Model**

- Explain the **client–server architecture**
- Identify:

  - Client as the request initiator (browser / frontend)
  - Server as the request processor (backend)

- Describe request–response flow at a high level
- Understand how frontend and backend communicate over the network

---

### **6. Get an Overview of 3-Tier Architecture**

- Identify the three tiers in a typical web application:

  - Presentation Layer (Frontend)
  - Application Layer (Backend)
  - Data Layer (Database)

- Understand the responsibilities of each tier
- Explain why separating concerns improves:

  - Scalability
  - Maintainability
  - Security

---

### **7. Understand the Need for JavaScript on the Server**

- Recall that JavaScript traditionally ran only in the browser
- Explain why JavaScript required:

  - A JavaScript engine
  - Browser-provided APIs (Web APIs)

- Analyze the problem of running JavaScript outside the browser

---

### **8. Trace the Origin and Purpose of Node.js**

- Understand early attempts to run JavaScript outside the browser
- Identify **Node.js (2009)** as the successful solution
- Explain at a high level:

  - How Node.js enabled JavaScript to run on servers
  - Why this unified frontend and backend languages

- Recognize key reasons for Node.js popularity:

  - Single language across stack
  - Non-blocking, event-driven nature (conceptual only)
  - Large ecosystem and community adoption

---

### **9. Build Conceptual Readiness for Backend Development**

- Develop a mental model of how:

  - Frontend applications depend on backend systems
  - Backend governs application behavior and data

- Prepare for upcoming sessions on:

  - Node.js internals
  - Modular systems
  - Express and API development

---

## **End-of-Session Outcome**

By the end of Node.js Day 1, students will:

- Clearly understand **why backend exists**
- Know **what problems backend solves**
- Be able to articulate **why frontend-only solutions do not scale**
- Be mentally prepared to learn **Node.js as a backend runtime**

---
