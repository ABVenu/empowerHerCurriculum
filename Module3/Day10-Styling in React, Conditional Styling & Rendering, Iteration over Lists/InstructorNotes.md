# Styling in React, Conditional Styling & Rendering, Iteration over Lists

These notes introduce various ways to style components in React, how to apply conditional styling and rendering, the nullish coalescing operator, iterating lists with keys, and a few other commonly used patterns. Components, props, `useState`, and `useEffect` are assumed as known.

---

# 1. Styling in React

React supports multiple approaches to styling. Each has trade-offs in scope, maintainability, and ease of use.

---

## 1.1 Global CSS

Global styles are defined in `.css` files and imported once in your app (usually `index.js` or the component where needed).

### Example

```css
/* styles.css */
.container {
  padding: 20px;
  background-color: #f0f0f0;
}
```

```jsx
import "./styles.css";

function App() {
  return <div className="container">Hello</div>;
}
```

### When to Use

* When styles are shared across multiple components.
* For global resets, typography, and layout.

### Limitations

* Styles can unintentionally leak and override other component styles.

---

## 1.2 CSS Modules (Modular CSS)

CSS Modules scope styles **locally** to a component. Helps avoid naming collisions.

### Example

```css
/* Button.module.css */
.btn {
  padding: 10px;
  background-color: blue;
  color: white;
}
```

```jsx
import styles from "./Button.module.css";

function Button() {
  return <button className={styles.btn}>Click</button>;
}
```

### Advantages

* Automatically scoped class names.
* Better maintainability in larger projects.

---

## 1.3 Inline Styling

Inline styles are applied directly via the `style` prop.
React uses **JS objects**, not CSS strings.

### Example

```jsx
function Box() {
  return (
    <div style={{ padding: "20px", backgroundColor: "lightgray" }}>
      Box
    </div>
  );
}
```

---

## 1.4 Why Double Curly Braces `{{ }}` in Inline Styles?

* The outer `{}` tells React: "this is JavaScript inside JSX".
* The inner `{}` is the **JavaScript object** containing style properties.

Example breakdown:

```jsx
<div style={{ color: "red" }}>
```

```bash
`style={ ... }` → JavaScript expression
`{ color: "red" }` → object literal
```

---

## 1.5 Combining CSS Approaches

Often, projects mix methods:

* Global CSS for resets.
* Modules for component-level styles.
* Inline for dynamic styles computed at runtime.

---

# 2. Conditional Styling

Conditional styling means applying classes or styles based on component state or props.

### Example 1: Conditional Class

```jsx
<div className={isActive ? "active" : "inactive"}>
  Status
</div>
```

### Example 2: Conditional Inline Style

```jsx
<div style={{ color: count > 5 ? "green" : "red" }}>
  {count}
</div>
```

### Example 3: Merging Class Names

```jsx
<div className={`btn ${isDisabled ? "disabled" : ""}`}>
```

---

# 3. Conditional Rendering

React allows rendering elements conditionally based on logic.

## 3.1 Using Ternary

```jsx
{isLoggedIn ? <Dashboard /> : <Login />}
```

## 3.2 Using Logical AND (`&&`)

```jsx
{show && <p>Visible only when show is true</p>}
```

## 3.3 Using Logical OR (`||`)

```jsx
<p>{username || "Guest"}</p>
```

## 3.4 Returning `null`

A component can return `null` to render nothing.

```jsx
if (!shouldShow) return null;
```

---

# 4. Nullish Coalescing Operator (`??`)

This operator returns the **right side only if the left side is null or undefined**.

More predictable than `||`, which treats many values (0, "", false) as falsy.

### Example

```jsx
const username = null;
<p>{username ?? "Guest"}</p>   // Output: Guest
```

### Comparison with OR (`||`)

```jsx
const count = 0;
<p>{count || 10}</p>   // Output: 10 (undesired)
<p>{count ?? 10}</p>   // Output: 0 (desired)
```

---

# 5. Iteration of Lists & React Keys

Iterating lists is common when rendering dynamic UI from arrays.

## 5.1 Basic List Rendering

```jsx
const users = ["A", "B", "C"];

<ul>
  {users.map((user) => (
    <li>{user}</li>
  ))}
</ul>
```

## 5.2 Why Keys Are Needed

Keys help React identify which items changed, added, or removed.

They must be:

* Unique within the list
* Stable (not index-based unless unavoidable)

## 5.3 Correct Use

```jsx
users.map((user) => (
  <li key={user.id}>{user.name}</li>
));
```

## 5.4 When You Should Avoid Index as Key

* When list items reorder
* When items are added/removed

Index can be used when:

* List never changes
* Static and short list

---

# 6. Additional Useful React Topics

These often come up while teaching beginners.

---

## 6.1 Fragments (`<></>`)

Used to group elements without creating extra DOM nodes.

```jsx
<>
  <h1>Title</h1>
  <p>Description</p>
</>
```

---

## 6.2 Default Props (for function components)

```jsx
function Button({ text = "Click" }) {
  return <button>{text}</button>;
}
```

---

## 6.3 Passing Functions as Props

```jsx
function Child({ onClick }) {
  return <button onClick={onClick}>Click</button>;
}
```

---

## 6.4 Controlled vs Uncontrolled Inputs

### Controlled Input - (In Upcoming Session, that is useRef)

```jsx
const [name, setName] = useState("");

<input value={name} onChange={(e) => setName(e.target.value)} />
```

### Uncontrolled Input

```jsx
<input ref={inputRef} />
```

---



---

# 7. Best Practices Summary

* Prefer CSS Modules for component isolation.
* Use inline styles only for dynamic or computed values.
* Use conditional rendering patterns to make components expressive.
* Use `??` over `||` when dealing with values like 0 or empty strings.
* Always provide unique, stable keys when rendering lists.
* Avoid unnecessary re-renders by not deriving state that can be computed.

---

