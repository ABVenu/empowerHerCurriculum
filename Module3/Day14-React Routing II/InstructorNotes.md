

# React Routing — 2 (Dynamic & Protected Routes)

### Session Goal

Learners understand **dynamic routing** and **protected routes**, using authentication state managed via **Context API or localStorage**.

---

## What to Cover in React Routing — 2

### Dynamic Routes

* Routes with parameters
* URL carries dynamic data
* Real-world examples:

  * User profile pages
  * Product detail pages

---

### Reading Route Parameters

Introduce clearly:

* **useParams**

  * Extracts dynamic values from the URL
  * Allows components to respond to URL data

---

### Protected Routes (Core Focus of Session 2)

Explain conceptually:

* Some routes should not be accessible to everyone
* Access depends on authentication state

---

### Authentication State Sources

Explain anyone approaches:

* **Context API**

  * Auth state stored globally
  * Preferred approach

* **localStorage** - better go with this

  * Auth persistence across reloads
  * Used together with Context

---

### Redirecting Unauthorized Users

Introduce term clearly:

* **Navigate**

  * Used to redirect users
  * Handles conditional route access

(Conceptual usage only)

---

### Real-World Protected Route Examples

Examples to be implemented in practice:

* Dashboard page
* Profile page
* Admin page

---

### Routing Best Practices (Beginner Level)

* Keep route definitions centralized
* Name routes meaningfully
* Avoid unnecessary route complexity
* Use protected routes sparingly

---

### Expected Outcome After Routing — 2

Learners should be able to:

* Use dynamic routes
* Read URL parameters
* Understand protected routes
* Control access based on auth state
* Build basic auth-aware navigation

---

