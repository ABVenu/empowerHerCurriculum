### **Authentication**

## **Learning Objectives**
By the end of this session, students will be able to:

---

## **1.0 Understand the Need for Security Measures and Backend Responsibility**

---

## **1.1 Why Security Measures Are Needed**

- Understand risks involved in backend systems such as:

  - Unauthorized access
  - Data leaks
  - Account compromise

- Understand how insecure systems impact users and businesses

- Recognize security as a **core backend responsibility**

---

## **1.2 Why Security Is the Responsibility of the Backend**

- Understand that frontend code is:

  - Public
  - Easily inspectable
  - Modifiable by users

- Understand why sensitive logic must never be handled on the frontend

- Identify backend as the trusted layer for:

  - Identity verification
  - Credential validation

---

## **1.3 Types of Security Measures Required in Backend Systems**

- Identify different security measures required at the backend level such as:

  - Secure password storage
  - Authentication checks
  - Controlled access to sensitive operations

- Understand that security is not a single feature but a set of practices

---

## **1.4 Understand the Difference Between Hashing and Encryption**

- Define **hashing** as a one-way transformation

- Define **encryption** as a two-way transformation

- Understand why passwords must be:

  - Hashed
  - Never encrypted or stored in plain text

- Relate hashing to real-world password security

---

## **2.0 Hashing and Comparing Passwords (Signup & Login)**

---

## **2.1 Understand Why Password Hashing Is Required**

- Understand why raw passwords must never be stored
- Identify risks of storing plain-text passwords
- Understand how hashing protects users even if the database is compromised

---

## **2.2 Implement Password Hashing During Signup**

- Understand **bcrypt** as a password hashing library
- Hash user passwords before storing them in the database
- Store only hashed passwords in the database
- Understand the role of salt in secure hashing

---

## **2.3 Implement Password Comparison During Login**

- Compare user-provided passwords with stored hashed passwords
- Understand why hashed passwords cannot be directly compared
- Implement secure login validation logic
- Handle invalid login attempts safely

---

## **3.0 Build Signup and Login Routes**

---

## **3.1 Implement Signup Route**

- Accept user credentials securely
- Validate input data
- Hash password and store user details in the database
- Return appropriate responses for success and failure cases

---

## **3.2 Implement Login Route**

- Accept login credentials
- Retrieve user details from the database
- Compare hashed password with user input
- Allow or deny login based on password verification

---

## **3.3 Understand the Limitations of This Authentication Setup**

- Understand that authentication currently:

  - Verifies identity only at login time
  - Does not maintain user session

- Recognize the need for additional mechanisms for protected routes

- Prepare conceptually for authorization and token-based systems in the next session

---

## **End-of-Session Outcome**

By the end of this session, students will:

- Understand why backend security is critical
- Securely store user passwords using hashing
- Implement signup and login functionality
- Compare hashed passwords safely
- Build a basic authentication system without tokens
- Be ready to extend authentication with authorization mechanisms next
