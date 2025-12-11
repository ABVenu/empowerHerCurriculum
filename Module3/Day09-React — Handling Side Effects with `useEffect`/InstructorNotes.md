# **Learning Objectives: React — Handling Side Effects with `useEffect`**

---

## **Understand What Side Effects Are in React**

- Define what a **side effect** is and why certain operations cannot be done directly in the render phase.
- Identify common side-effect scenarios:
  API calls, subscriptions, timers, DOM manipulation, event listeners.

---

## **Explain What `useEffect` Is and Why It Is Used**

- Describe the purpose of `useEffect` in managing side effects safely.
- Demonstrate how React runs effects **after rendering**, ensuring consistent UI updates.
- Compare `useEffect` with component lifecycle methods (`componentDidMount`, `componentDidUpdate`, `componentWillUnmount`).

---

## **Use `useEffect` Through Practical Examples**

- Implement an effect that logs messages when a component renders.
- Fetch API data using `useEffect` and store it in state.
- Create a timer or interval inside `useEffect` and clean it up when the component unmounts.

---

## **Use the `useEffect` Syntax with Different Dependency Array Cases**

- Write a basic `useEffect` with **no dependencies** (runs on every render).
- Use an effect with an **empty dependency array** (runs only once — mount behavior).
- Use an effect with **dependencies in the array** (runs only when the dependencies change).
- Explain how **multiple dependencies** influence re-renders and data updates.

---

## **Work With Multiple `useEffect` Hooks**

- Write a component that uses multiple distinct effects for different tasks.
- Maintain separation of concerns by grouping related side effects into separate `useEffect` blocks.

---

## **Identify Common Pitfalls and Best Practices for `useEffect`**

- Avoid writing state updates or props-based calculations that cause **infinite render loops**.
- Explain why functions, objects, and arrays in dependencies must be handled carefully (reference equality issues).
- Use the **rules of hooks** correctly (not inside loops, conditions, or nested functions).
- Follow best practices for dependency arrays, readability, and clarity.

---

## **Explain Cleanup Functions in `useEffect`**

- Describe the purpose of cleanup functions in preventing memory leaks.
- Implement cleanup for:

  - intervals
  - timeouts
  - event listeners
  - subscriptions

- Connect cleanup logic to the lifecycle equivalent of `componentWillUnmount`.

---

## **Understand Component Lifecycle Through `useEffect`**

- Map how `useEffect` represents all class component lifecycle phases:

  - **Mount** (empty dependency array)
  - **Update** (dependencies)
  - **Unmount** (cleanup function)

- Predict how effects will run during the lifecycle based on dependency changes.

---
