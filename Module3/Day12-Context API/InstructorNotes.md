# React — Context API

These notes introduce the **Context API** as a solution to two common problems in React applications: **props drilling** and the **need for shared (global) state management**. Learners are expected to understand components, props, state, `useState`, `useEffect`, and `useRef`. The focus is on **conceptual clarity**, **problem identification**, and **simple, real-world use cases** to be implemented during practice sessions.

---

# 1. Why Context API Is Needed

As React applications grow, managing and sharing data across components becomes difficult.
Context API addresses **two fundamental problems** that arise in such situations.

---

## 1.1 Problem 1: Props Drilling

Props drilling occurs when:

- Data is owned by a top-level component
- Many deeply nested components need the same data
- Intermediate components pass props without using them

This results in:

- Tight coupling between components
- Reduced readability
- Difficult maintenance as the app grows

---

## 1.2 Problem 2: Need for Global State Management

Some data in an application is **global by nature**, meaning:

- It is needed by many unrelated components
- It should remain consistent across the app
- It represents the overall state of the application

Examples of global data:

- Logged-in user information
- Authentication status
- Theme (light / dark)
- Language or user preferences

Managing such data only with props becomes impractical.

---

# 2. What Context API Is (Conceptually)

Context API provides a way to:

- Create shared state
- Store application-level or feature-level data
- Allow components to access this data directly

Context acts as a **central data source** for a group of components, without turning every value into a prop.

---

## 2.1 Context vs Local State

Important distinction:

- **Local state** belongs to a single component
- **Context state** is shared across multiple components

Context does not replace local state; it complements it.

---

# 3. Core Building Blocks of Context API

Context API works through three conceptual steps.

---

## 3.1 Creating Context

This step defines **what data will be shared globally**.

Examples to be implemented:

- A context for authentication state
- A context for theme settings
- A context for application-wide preferences

---

## 3.2 Providing Context

A Provider:

- Supplies the shared data
- Wraps the part of the component tree that needs access
- Controls the scope of the global state

Examples to be implemented:

- Wrapping the entire app with a User Provider
- Wrapping only a section of the app with a Theme Provider

---

## 3.3 Consuming Context

Components inside the Provider:

- Access the shared data directly
- React to changes in global state
- Avoid receiving unnecessary props

Examples to be implemented:

- Navbar displaying user information
- Button switching theme
- Profile page accessing global user data

---

# 4. Simple Real-World Examples to Implement (Not all to demonstarte, Which One to Demonstarte is wrriten at last)

---

## 4.1 Theme as Global State

Scenario:

- Theme preference is needed in many components
- Multiple components must update when theme changes

Using Context:

- Theme is stored once
- All subscribed components stay in sync

---

## 4.2 Authentication as Global State

Scenario:

- Login status affects routing, UI, and access control
- Many components depend on authentication state

Using Context:

- Authentication state is centralized
- Components consume auth status directly

---

## 4.3 App Settings or Preferences

Scenario:

- User-selected settings affect UI across the app

Using Context:

- Settings are managed as shared global state
- Updates propagate automatically

---

# 5. Data Flow with Context API

Key rules:

- Data flows from Provider to consumers
- Updating context value re-renders subscribed components
- Only components that use the context respond to changes

This ensures predictable and controlled updates.

---

# 6. Relationship with Other State Management Approaches

Context API:

- Is built into React
- Handles simple to medium global state needs

It is suitable **before** introducing heavier solutions like Redux.

---

#### Demonstrate Theme for Props Drilling and Simple Todo CRUD for Global state managaement as application of Context API

# 7. Best Practices Summary

- Use Context to solve props drilling and global state needs.
- Keep contexts focused on a single concern.
- Avoid placing too much unrelated data in one context.
- Do not replace simple props with Context unnecessarily.
- Use local state where sharing is not required.

---

# 8. End-of-Session Learning Outcomes

By the end of this session, learners will be able to:

- Explain props drilling and why it is problematic
- Describe what global state is and why it is needed
- Explain how Context API solves both problems
- Identify scenarios suitable for Context
- Design simple Context-based solutions conceptually

---
