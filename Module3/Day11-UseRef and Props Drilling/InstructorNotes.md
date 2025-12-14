## UseRef and Props Drilling

## Learning Objectives

# React — `useRef` & Props Drilling

These notes introduce the purpose and usage of the `useRef` hook and explain the concept of props drilling in React. Learners are expected to already understand components, props, state (`useState`), and basic rendering behavior. The session focuses on **why certain problems occur**, **what tools React provides**, and **how to reason about them**, rather than advanced patterns.

---

# 1. `useRef` in React

`useRef` is a React Hook that allows you to store values that **persist across renders** without causing the component to re-render when the value changes.

---

## 1.1 Why `useRef` Is Needed

Not all values in a React component should trigger a UI update.

Some values:

- Need to be remembered across renders
- Should not cause re-rendering
- Are related to DOM elements rather than UI state

`useRef` helps handle these cases safely.

---

## 1.2 What `useRef` Is

- `useRef` returns an object with a single property: `.current`
- The value inside `.current` persists between renders
- Updating `.current` does **not** trigger a re-render

Basic syntax:

```jsx
const myRef = useRef(initialValue);
```

Accessing the value:

```jsx
myRef.current;
```

---

## 1.3 `useRef` vs `useState`

| Aspect                        | useState | useRef |
| ----------------------------- | -------- | ------ |
| Triggers re-render            | Yes      | No     |
| Value persists across renders | Yes      | Yes    |
| Used for UI updates           | Yes      | No     |
| Used for DOM access           | No       | Yes    |

Use `useState` when UI should update.
Use `useRef` when UI should **not** update.

---

## 1.4 Accessing DOM Elements Using `useRef`

React discourages direct DOM manipulation using selectors like `document.getElementById`.

Instead, refs are used.

### Example: Focusing an Input

```jsx
const inputRef = useRef(null);

<button onClick={() => inputRef.current.focus()}>
  Focus Input
</button>

<input ref={inputRef} />
```

---

## 1.5 Common Use Cases of `useRef`

`useRef` is commonly used for:

- Accessing DOM elements
- Storing previous values
- Storing timers or interval IDs
- Counting renders
- Holding mutable values that should not affect UI

---

## 1.6 `useRef` and Re-rendering Behavior

Important points:

- Changing `ref.current` does not re-render the component
- The ref value remains the same across renders
- Refs should not be used to store values that affect what is displayed on the screen

---

# 2. Introduction to Props Drilling

Props drilling refers to the process of passing data from a parent component to deeply nested child components through intermediate components that do not need the data.

---

## 2.1 What Is Props Drilling

When data flows like this:

```text
Parent → Child → Grandchild → DeepChild
```

and each component passes props forward, even if it doesn’t use them, this is called **props drilling**.

---

## 2.2 Why Props Drilling Becomes a Problem

Props drilling is not an error, but it creates problems as applications grow:

- Components receive props they don’t use
- Code becomes harder to read and maintain
- Small changes require updates in many files
- Component reusability decreases

---

## 2.3 Identifying Props Drilling

Props drilling can be identified when:

- Multiple components pass the same prop
- Intermediate components only forward props
- A deeply nested component depends on top-level state

---

## 2.4 Props Drilling as a Design Limitation

Important understanding for learners:

- Props drilling works fine for small apps
- It becomes problematic in larger component trees
- React provides better solutions for this problem

This section intentionally **does not introduce the solution yet**.

---

# 3. Conceptual Link to Upcoming Topics

This session prepares learners for upcoming concepts:

- `useRef` helps understand **non-rendering values**
- Props drilling introduces a **data-sharing problem**
- The next session (Context API) will address this problem directly

Learners should leave this session understanding **why a new tool is needed**, not just how to use it.

---

# 4. End-of-Session Learning Outcomes

By the end of this session, learners will be able to:

- Explain when `useRef` should be used instead of `useState`
- Use `useRef` to access DOM elements safely
- Describe how React handles re-rendering
- Identify props drilling in a component hierarchy
- Explain why props drilling becomes difficult to manage

---

# 5. Best Practices Summary

- Use `useRef` for values that should persist without causing re-renders.
- Avoid direct DOM manipulation using browser APIs.
- Do not use refs to manage UI state.
- Keep props passing shallow where possible.
- Recognize props drilling early before the component tree grows.
- Understand the problem clearly before learning the solution (Context API).

---

If you want, next I can:

- Prepare **Context API notes in the same format**
- Create **PSC problem statements** for `useRef`
- Convert this into **student-facing vs instructor-facing notes**

Just let me know.
