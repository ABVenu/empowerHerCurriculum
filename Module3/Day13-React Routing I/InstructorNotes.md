# React Routing — 1 

### Session Goal

Learners understand **what routing is**, **why it is needed**, and **how URLs map to components**, including handling **invalid routes (404)**.

---

## What to Cover in React Routing — 1

### Why Routing Is Needed in React

* React apps are **Single Page Applications (SPA)**
* Page does not reload; only components change
* URL represents **current view**
* Difference between:

  * Traditional multi-page apps
  * Client-side routing

---

### What React Router Is

* React Router is a **routing library**
* Not part of core React
* Handles:

  * URL changes
  * Component rendering based on URL

---

### Core Routing Terminology (Explicit & Clear)

Clearly introduce and define:

* **BrowserRouter**

  * Enables routing in the app
  * Listens to browser URL changes

* **Routes**

  * Container for all route definitions

* **Route**

  * Maps a path to a component

---

### Creating Basic Routes

* Home route (`/`)
* About route
* Contact route
* One path → one component

Explain route matching in simple terms.

---

### Navigation Components

Introduce navigation-related terms clearly:

* **Link**

  * Used for navigation without page reload
  * Replaces `<a>` tag

* **NavLink**

  * Same as Link
  * Can detect active route
  * Used for navigation menus

Explain:

* Why `<a>` tags should be avoided in React apps

---

### Layout Concept (Basic)

* Header / Navbar stays constant
* Page content changes
* Routing controls **what renders where**

(No nested routing yet)

---

### Handling 404 / Not Found Routes

* What happens when a route does not exist
* Why 404 handling is important
* Fallback route concept
* User experience importance

---

### Common Beginner Mistakes

* Forgetting to wrap app with BrowserRouter
* Using `<a>` instead of Link/NavLink
* Expecting full page reload
* Misunderstanding URL vs component rendering

---

### Expected Outcome After Routing — 1

Learners should be able to:

* Explain what routing is
* Use BrowserRouter, Routes, and Route
* Navigate using Link and NavLink
* Handle invalid routes (404)
* Build a simple multi-page React app

---