## React Fundamentals

### **Learning Objectives**

### 🔑 Prerequisites

Learners should already know:

- Basics of **HTML**, **CSS**, and **JavaScript**
- ES6 fundamentals (let/const, arrow functions, template literals)
- DOM basics and event handling in JS

---

#### Drawbacks of Traditional DOM Manipulation

- Frequent **reflow & repaint** during updates → **performance bottlenecks**
- **Imperative** UI updates → complex logic & harder to maintain
- UI may become **out of sync** with underlying application state
- Hard to scale for large and dynamic applications

---

#### How React Solves These Issues

- Uses **Virtual DOM (VDOM)** → reduces costly real DOM updates
- Only **updates the changed parts** of UI → smarter, faster rendering
- **Component-based** design → reusable, structured UI development
- **One-way data flow** → predictable state-driven UI updates
- **Declarative approach** → focus on “what UI should look like”

---

#### Virtual DOM Fundamentals

- A **lightweight, in-memory representation** of the actual DOM
- React creates **new VDOM** for every UI change
- Efficient **comparison (diffing)** between new & previous VDOM
- Changes are **selectively applied** to real DOM for optimization

---

#### React Diffing Algorithm & Reconciliation

- Determines the **smallest required update** to real DOM
- Avoids re-rendering entire UI → **minimized DOM operations**
- Uses **keys** in lists to track elements efficiently during updates

---

#### What is a React Element?

- A **plain JavaScript object** that describes UI structure
- Created using **JSX** or `React.createElement()`
- Represents **what UI should be**, not the actual DOM element
- **Immutable** → React replaces it instead of modifying directly

---

#### Key React Terminologies

- **VDOM, Diffing, Reconciliation** → Core behind-the-scenes engine (Explain in Detail in Depth)
- **Component** → Independent, reusable UI building blocks (Explain Briefly)
- **Props** → How components **communicate** with each other (Explain Briefly)
- **State** → Data that **changes over time** within a component (Explain Briefly)
- **JSX** → Allows writing HTML-like syntax inside JavaScript (No Need to explain in thi session)
- **Rendering / Mounting / Update cycle** → Lifecycle of UI elements (Only Explain Rendering)

---
