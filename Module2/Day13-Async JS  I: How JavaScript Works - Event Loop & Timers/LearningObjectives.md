# **Async JS  I: How JavaScript Works - Event Loop & Timers**

#### Learning Objectives

### **1. JavaScript as a Single-Threaded Language**

* Understand that JavaScript runs on a single call stack
* Identify what “single-threaded execution” means
* Recognize the limitations of a single-thread model

---

### **2. Overview of Multi-Threaded Languages**

* Understand how multi-threaded languages execute tasks in parallel
* Identify threads and shared memory at a high level
* Compare multi-threaded vs single-threaded execution

---

### **3. Blocking Code (Synchronous Execution)**

* Understand what blocking code means
* Observe how long-running tasks freeze JavaScript execution
* Identify why blocking is a problem in UI and server environments

---

### **4. How JavaScript Handles Multiple Tasks Non-Blocking**

* Understand what non-blocking behavior means
* Recognize that JS achieves non-blocking execution using the environment (Web APIs / Node APIs)
* Identify how JS delegates tasks to the runtime
* Understand the separation between JS engine vs external APIs

---

### **5. The Event Loop**

* Understand the role of the event loop in asynchronous execution
* Identify how the call stack, Web APIs, and callback/task queue interact
* Understand how the event loop continuously checks and transfers tasks
* Recognize why the event loop is essential for non-blocking behavior

---

### **6. Timers in JavaScript (No Promises, No Callbacks Topic Yet)**

* Understand how `setTimeout` is scheduled through Web APIs
* Understand how `setInterval` repeats tasks through the event loop
* Identify that timer delays are queued, not guaranteed precise execution
* Understand that timer functions run only when the call stack is empty

---
