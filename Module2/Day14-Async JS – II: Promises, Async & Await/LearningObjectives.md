
# **Async JS – II: Promises, Async & Await**

## **Learning Objectives**

### **1. Why We Need a System Like Promises**

* Understand limitations of using only callbacks to handle async tasks
* Recognize that async tasks may succeed or fail
* Understand the need for a mechanism that *watches* an async task and reports:

  * **fulfilled (resolved)**
  * **rejected (error)**
* Identify how Promises solve execution-after-async-completion problems

---

### **2. Introduction to Promises**

* Understand what a Promise represents
* Understand the three states: pending, fulfilled, rejected
* Use `setTimeout` as a simple async task for Promise examples
* Use `.then()` for handling resolved values
* Use `.catch()` for handling errors
* Use `.finally()` for cleanup actions

---

### **3. Writing Async Code with Async–Await**

* Understand why async–await is a cleaner way to write async code
* Convert Promise-based code to async–await
* Use `try–catch` with async–await for error handling
* Understand that async–await is built on top of Promises

---

### **4. Additional Promise Concepts (Overview Only)**

* Understand `Promise.all` for running tasks in parallel
* Understand `Promise.allSettled` for getting all results, even if some fail
* Understand `Promise.race` for first-completed task behavior
* Recognize real-world use cases

---

### **5. Applying Callbacks Inside Promises**

* Understand how Promises still use callbacks internally (`then`, `catch`)
* Trace execution flow: async task → Promise → then/catch callback
* Recognize the transition from callback-style async to promise-style async
