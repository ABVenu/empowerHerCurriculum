### React — State Management with `useReducer`

# **Learning Objectives:**

---

## **Understand the Need for Structured State Management**

- Identify situations where using multiple `useState` hooks becomes difficult to manage.
- Recognize patterns where several pieces of state change together.
- Explain why scattered state update logic reduces readability and maintainability.

---

## **Explain What `useReducer` Is and Why It Is Used**

- Describe `useReducer` as an alternative to `useState` for managing complex state.
- Explain how `useReducer` centralizes state update logic in one place.
- Compare `useReducer` with `useState` in terms of use cases and complexity.

---

## **Understand the Core Concepts of `useReducer`**

- Define the key concepts involved in `useReducer`:

  - state
  - action
  - reducer function

- Explain how actions describe **what happened**, not **how state changes**.
- Describe how the reducer determines the next state based on the current state and action.

---

## **Use `useReducer` Through Practical Scenarios**

- Manage form state using `useReducer`.
- Handle multiple related state values with predictable updates.
- Use `useReducer` for UI state such as toggles, counters, or step-based flows.

---

## **Understand the Data Flow in `useReducer`**

- Trace the flow from user interaction to state update:

  - UI event → dispatch action → reducer → new state → UI update

- Explain why this flow makes state transitions easier to reason about.
- Identify how `useReducer` improves debugging and predictability.

---

## **Refactor Existing `useState` Logic to `useReducer`**

- Convert a component using multiple `useState` hooks into a `useReducer` implementation.
- Identify which parts of the logic move into the reducer function.
- Compare readability and maintainability before and after refactoring.

---

## **Identify When to Use and When Not to Use `useReducer`**

- Choose `useReducer` when:

  - State logic is complex
  - Multiple values depend on each other
  - State transitions are frequent or structured

- Avoid `useReducer` when:

  - State is simple
  - A single `useState` is sufficient

---

## **Follow Best Practices for `useReducer`**

- Keep reducer functions pure and predictable.
- Avoid side effects inside reducers.
- Use meaningful action descriptions.
- Maintain clear separation between UI logic and state update logic.

---

## **Understand the Relationship Between `useReducer` and Other React Concepts**

- Explain how `useReducer` works alongside:

  - `useState`
  - Context API

- Understand how `useReducer` prepares learners for larger applications and structured state management.

---
