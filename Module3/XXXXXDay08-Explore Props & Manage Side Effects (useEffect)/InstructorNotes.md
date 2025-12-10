## Explore Props & Manage Side Effects (useEffect)

### Learning Objectives
---

#### 1️⃣ Why More Components?

- UI should be divided into **small, reusable** components
- Each component should handle **one specific responsibility**
- Better **maintainability** and easier collaboration in teams

👉 Smaller components = cleaner + scalable UI

---

#### 2️⃣ What are Props?

- **Props** = data passed **from parent component → child component**
- Help components **communicate**
- Make components **dynamic** and **reusable**

Characteristics of Props:

- **Read-only / Immutable** → cannot be modified by child
- **Unidirectional Flow** → parent → child only
- Used to **customize** components with different values

Activity:

- Create a `Greeting` component
- Pass student name through props from `App.jsx`
- Display: `"Hello, Sanidhya! Welcome to React!"`

👉 Props let components **share data** without direct DOM manipulation

---

#### 3️⃣ Why State is Not Enough?

- State handles **UI changes internally**
- But sometimes **state change must trigger extra behavior**
  Example:

  - Show popup when count hits a value
  - Fetch data from server when component loads

Such actions are called **Side Effects**

---

#### 4️⃣ What are Side Effects?

- Any operation **outside** the normal UI rendering flow:

  - Alerts
  - Timers
  - Data fetching
  - Logging to console
  - Updating browser title

👉 Side effects should be controlled properly

---

#### 5️⃣ Introducing `useEffect()`

- A **Hook** used to perform side effects in components
- Executes **after** React renders the UI

Basic Syntax:

```js
useEffect(() => {
  // side effect code here
});
```

---

#### 6️⃣ Simple useEffect Example

**Scenario:**
Button click → increases count
Whenever `count % 5 === 0`, show an alert

Key learning:

- Updates UI with `useState()`
- `useEffect()` reacts to **state change**

Explanation:

- State changes → trigger re-render
- After render → `useEffect()` executes side effect logic

👉 Students now understand how React **manages UI changes + extra actions** cleanly

---

### 🎯 Expected Outcome of Session 3

By the end of this session, students can:

✔ Break UI into smaller components
✔ Pass & use props correctly
✔ Understand props characteristics (immutable)
✔ Explain what side effects are
✔ Use `useEffect()` for state-based actions

---
