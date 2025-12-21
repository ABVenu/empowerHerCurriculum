### Performance Optimization — I

# **Learning Objectives:**

---
#### [Earlier Video For Ready Ref](https://live.masaischool.com/embed/video/511942b6-b47b-4280-a7db-4dffd2736b49)
## **Understand the Need for Performance Optimization**

- Explain what performance means in a React application.
- Identify common symptoms of performance issues:

  - Slow UI updates
  - Lag during interactions
  - Unnecessary re-renders

- Understand why performance problems become more visible as applications grow.
- Emphasize that optimization is required **only when performance issues exist**.

---

## **Understand React Re-rendering Behavior**

- Explain what causes a React component to re-render.
- Understand how state and props changes affect re-rendering.
- Identify how parent re-renders can impact child components.
- Connect unnecessary re-renders to performance degradation.

---

## **Introduce Core Performance Optimization Tools**

- List the primary performance optimization tools in React:

  - `useMemo`
  - `useCallback`
  - `React.memo`
  - Lazy loading

- Understand that each tool solves a **different performance problem**.
- Identify which tools will be explored in depth and which will be introduced conceptually.

---

## **Deep Dive: `useMemo`**

- Explain what `useMemo` is and why it is used.
- Understand how expensive computations affect render performance.
- Identify scenarios where derived values are recalculated unnecessarily.
- Explain how `useMemo` memoizes values based on dependencies.

---

## **Use `useMemo` Through Practical Demonstration**

- Optimize expensive calculations using `useMemo`.
- Prevent unnecessary recomputation during re-renders.
- Compare component behavior before and after applying `useMemo`.

---

## **Deep Dive: `useCallback`**

- Explain why functions are recreated on every render.
- Understand how changing function references affect child components.
- Explain how `useCallback` memoizes function references.
- Identify scenarios where `useCallback` improves performance.

---

## **Use `useCallback` Through Practical Demonstration**

- Stabilize function references when passing them as props.
- Prevent unnecessary child component re-renders.
- Compare component behavior with and without `useCallback`.

---

## **Identify When to Use and When Not to Optimize**

- Use optimization tools when:

  - Re-render issues are observed
  - Computations are expensive

- Avoid optimization when:

  - Logic is simple
  - Performance is already acceptable

- Understand the concept of **premature optimization**.

---

## **End-of-Session Expected Outcomes (Session I)**

By the end of this session, learners will be able to:

- Explain why performance optimization is needed
- Identify unnecessary re-renders
- Apply `useMemo` to optimize expensive computations
- Apply `useCallback` to stabilize function references
- Make informed decisions about basic performance optimizations

---
