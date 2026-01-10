## **Learning Objectives – Node.js (Session 2)**

By the end of this session, students will be able to:

---

## **1. Recall How JavaScript Executes in the Browser**

- Explain how JavaScript code is executed inside the browser
- Identify the major components involved in browser-based JS execution:

  - JavaScript Engine
  - Web APIs
  - Callback Queue
  - Event Loop

- Describe the role of:

  - Call Stack
  - Asynchronous APIs (timers, DOM events, network calls)

- Reinforce understanding of **single-threaded execution with asynchronous behavior**

---

## **2. Compare Browser JavaScript vs Server-Side JavaScript**

- Identify similarities between browser JS and Node.js JS:

  - Language syntax
  - Core execution model

- Identify key differences:

  - Availability of Web APIs
  - Environment responsibilities
  - Purpose of execution (UI vs business logic)

- Explain why browser-specific APIs (DOM, window, document) are unavailable in Node.js

---

## **3. Understand Node.js as a Runtime Environment**

- Define Node.js as a **JavaScript runtime**, not a framework
- Explain how Node.js:

  - Uses a JavaScript engine
  - Provides its own APIs to replace browser Web APIs

- Understand the role of Node.js in executing JavaScript on the server

---

## **4. Explain Node.js Architecture at a High Level**

- Identify the core components of Node.js architecture:

  - JavaScript Engine
  - Node.js Core APIs
  - Native bindings
  - Event loop

- Explain how JavaScript code interacts with lower-level system operations

---

## **5. Understand the Role of libuv in Node.js**

- Define **libuv** as the library responsible for:

  - Asynchronous I/O operations
  - Event loop implementation

- Identify operations handled by libuv, such as:

  - File system access
  - Networking
  - Timers

- Understand how libuv enables non-blocking behavior in Node.js
- Explain event loop with respect to NodeJS
  - Emphasize Macro Task Queue & Micro Task Queue

---

## **6. Understand Thread Pool and Worker Threads**

- Explain the concept of a **thread pool**
- Identify tasks delegated to the thread pool:

  - File system operations
  - Cryptographic tasks

- Understand why Node.js is still considered single-threaded despite using threads internally
- Get an introductory understanding of **worker threads** and their purpose

---

## **7. Understand Node.js Bindings**

- Explain the role of Node.js bindings in:

  - Connecting JavaScript code with native C/C++ implementations

- Understand how JavaScript APIs map to low-level system calls
- Appreciate why Node.js is performant despite being JavaScript-based

---

## **8. Understand the Node.js Module System**

- Define what a module is and why modularization is required
- Identify benefits of modular systems:

  - Code reusability
  - Maintainability
  - Separation of concerns

- Understand how Node.js supports modular programming

---

## **9. Differentiate Between CommonJS (CJS) and ES Modules (ESM)**

- Identify CommonJS as the traditional Node.js module system
- Identify ES Modules as the modern JavaScript module system
- Compare CJS and ESM in terms of:

  - Syntax (`require` vs `import`)
  - Export mechanisms
  - Execution behavior

- Demonstrate the same logic (e.g., `print1to10`) using both CJS and ESM

---

## **10. Evaluate Merits and Demerits of CJS and ESM**

- Analyze advantages and limitations of CommonJS
- Analyze advantages and limitations of ES Modules
- Understand ecosystem compatibility considerations
- Justify the decision to use **ES Modules consistently** for backend development

---

## **11. Explore Built-in Modules in Node.js**

- Identify built-in (internal) Node.js modules
- Understand the purpose of commonly used built-in modules:

  - `os` module for system-level information
  - `fs` module for file system operations

- Perform basic exploration of these modules and their capabilities

---

## **12. Prepare for Scalable Backend Development**

- Develop a clear mental model of how:

  - Node.js handles concurrency
  - Modular systems enable scalable backend codebases

- Build readiness for upcoming topics:

  - Package managers
  - External modules
  - Express framework and APIs

---

## **End-of-Session Outcome**

By the end of Node.js Day 2, students will:

- Understand **how Node.js works internally**
- Clearly differentiate **browser JS vs Node.js JS**
- Be comfortable with **Node’s architecture and async model**
- Write modular backend code using **ES Modules**
- Confidently explore and use **built-in Node.js modules**
