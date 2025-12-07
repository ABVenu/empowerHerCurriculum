## Cleanup Function in useEffect & Introduction to useRef

### Learning Objectives

---

#### 1️⃣ Component Lifecycle in React

Students will learn the basic lifecycle of a functional component:

- **Mount** → Component appears on screen for the first time
- **Update** → Component re-renders due to state/props change
- **Unmount** → Component is removed from the UI

👉 Some logic must run **during mount**, some **after update**, and some must be **cleaned up during unmount**

---

#### 2️⃣ Why Cleanup?

- Some side effects keep running in background:

  - Timers (setInterval)
  - Event listeners
  - Subscriptions

- If not cleaned → **memory leak ➜ performance issues**

👉 Cleanup ensures React removes or stops leftover work when component unmounts

---

#### 3️⃣ Cleanup Function in `useEffect()`

- `useEffect()` can return a function → **cleanup function**
- This function runs **before unmount** or **before the next effect runs again**

Basic example:

```js
useEffect(() => {
  console.log("Effect running");

  return () => {
    console.log("Cleanup happening");
  };
}, []);
```

Explanation:

- Useful for removing event listeners, clearing intervals, closing connections etc.

---

#### 4️⃣ Why do we need `useRef()`?

Students already know:

- `useState()` → stores **reactive** data (causes re-render)
- `useEffect()` → handles **side effects**

But some values:

- **Should not cause re-render**
- Need to be **persisted across renders**
- Need to directly access **DOM elements** (like input focus)

👉 That’s where `useRef()` helps!

---

#### 5️⃣ What is `useRef()`?

- Stores a **mutable value** that survives re-renders
- Updating `ref.current` **does NOT re-render**
- Can directly **access DOM nodes**

Example purposes:

- Remember previous state values
- Track number of renders
- Access HTML elements like `<input>` or `<video>`

---

#### 6️⃣ useRef() — Simple Examples

Example 1️⃣: Focus an input

- Add a button → When clicked → input gets focused
- Demonstrates **DOM element interaction**

Example 2️⃣: Video Controls

- Play / Pause video using `useRef`
- No re-render needed → perfect useRef use case

👉 Students see **clear difference** between state & ref usage

---

### 🎯 Expected Outcome of Session 4

By the end, students can:

✔ Explain component lifecycle (mount / update / unmount)
✔ Implement cleanup function in `useEffect()`
✔ Know when and why to use `useRef()`
✔ Use `useRef()` for direct DOM access and values that shouldn’t trigger re-render

---
