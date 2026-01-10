### **Session Name: Authorization**

## **Learning Objectives**

By the end of this session, students will be able to:

---

## **1.0 Understand What Authorization Means in Backend Systems**

---

## **1.1 Understand Why Authorization Is Required After Login**

- Recall that authentication only verifies **who the user is**

- Understand that authorization verifies **what the user is allowed to do**

- Identify the problem:

  - Login happens once
  - Backend must still identify the user on every request

- Understand the need for a mechanism that **proves the user has logged in**

---

## **1.2 Understand Why Backend Must Re-Verify Identity on Every Request**

- Understand that HTTP is **stateless**
- Recognize that backend does not remember users automatically
- Identify the need for a repeatable proof of identity
- Understand authorization as a **request-level security mechanism**

---

## **2.0 Understand Different Types of Authorization Mechanisms**

---

## **2.1 Token-Based Authorization**

- Understand token-based authorization as:

  - Client stores a token
  - Token is sent with every request

- Identify common use cases for token-based systems

- Understand why tokens work well for APIs and distributed systems

---

## **2.2 Session-Based Authorization**

- Understand session-based authorization using:

  - Server-side sessions
  - Session identifiers stored in cookies

- Identify where session-based auth is commonly used

- Understand limitations of session-based systems at scale

---

## **2.3 OTP-Based Authorization**

- Understand OTP-based authorization flow

- Identify OTP usage in:

  - Banking systems
  - High-security applications

- Understand why OTP is used as an additional verification layer

---

## **2.4 Compare Authorization Mechanisms**

- Compare Token-based, Session-based, and OTP-based authorization
- Identify advantages and limitations of each approach
- Understand why modern backend APIs prefer token-based authorization

---

## **3.0 Understand JSON Web Tokens (JWT)**

---

## **3.1 Define What a JWT Is**

- Define **JSON Web Token**
- Understand JWT as a compact, self-contained token
- Understand that JWT contains:

  - Header
  - Payload
  - Signature

---

## **3.2 Understand How JWT Works**

- Understand the lifecycle of a JWT:

  - Generated after successful login
  - Sent to the client
  - Included in subsequent requests
  - Verified by the backend

- Understand how JWT proves user identity without storing session data

---

## **3.3 Understand Why JWT Is Popular**

- Identify reasons for JWT popularity:

  - Stateless nature
  - Easy scalability
  - No server-side session storage
  - Works well with REST APIs

- Understand JWT usage in modern backend architectures

---

## **4.0 Demonstrate JWT-Based Authorization**

---

## **4.1 Generate JWT After Successful Login**

- Generate JWT after password verification
- Embed user identity inside the token payload
- Sign the token using a secret key
- Understand the importance of token expiration

---

## **4.2 Send JWT from Client to Backend**

- Understand how clients send JWT using HTTP headers
- Identify `Authorization` header and `Bearer` token format
- Understand why tokens should not be sent in request bodies

---

## **4.3 Verify JWT Using Authentication Middleware**

- Create authentication middleware in Express
- Extract token from request headers
- Verify token validity and signature
- Reject requests with:

  - Missing tokens
  - Invalid tokens
  - Expired tokens

---

## **4.4 Protect Backend Routes Using Middleware**

- Apply authentication middleware to protected routes
- Allow access only to authenticated users
- Attach verified user information to the request object
- Understand how middleware centralizes authorization logic

---

## **End-of-Session Outcome**

By the end of this session, students will:

- Clearly differentiate between authentication and authorization
- Understand multiple authorization mechanisms
- Explain what JWT is and how it works
- Justify why JWT is widely used in backend systems
- Generate and verify JWT tokens
- Protect backend routes using authentication middleware
- Build secure, production-ready backend APIs
