## Understanding Project Structure, Manage state - useState

### Learnig Objectives

---

#### 1️⃣ Create a React Project with Vite

Students will learn:

- Initialize a React app using **Vite**
- Run the development server
- Explore project structure:

  Files & folders to understand:

  - `index.html` → **root HTML container**
  - `main.jsx` → first JS entry point, renders React to DOM
  - `App.jsx` → **root component**
  - `assets/` → images & static files
  - `styles.css` / other CSS → styling structure
  - `package.json` → dependencies & scripts
  - `node_modules` → installed packages

---

#### 2️⃣ What is JSX?

Students will understand:

- JavaScript + XML syntax → **UI written like HTML inside JS**
- JSX → **More readable and faster to build UI**
- Browser doesn’t understand JSX → bundler **converts to JS**

Activity:

- Create a basic JSX component
- Display “**Welcome to React Session!**” inside DOM

Comparison Demo:

- Show how creating elements in JSX is **much simpler** than
  `document.createElement()` & manual DOM manipulation

👉 Convince them JSX is **declarative & developer-friendly**

---

#### 3️⃣ What is a Component?

Students will learn:

- A component = **reusable UI block**
- Function-based components
- How to **import & render components** inside `App.jsx`

Activity:

- Create 2 simple components (e.g., `Header`, `Footer`)
- Render inside `App.jsx`
- No props and no state here yet → just **structure**

👉 Emphasis: Components make UI **reusable, maintainable & structured**

---

#### 4️⃣ State Management — Why do we need State?

Students will understand:

- Static UI vs **Dynamic UI**
- Traditional DOM:

  - Data changes need **manual DOM manipulation**

- React:

  - UI automatically updates **when state updates**

Explain concept:

- State = **data that changes over time**
- If data changes → UI must reflect automatically

---

#### 5️⃣ Introducing `useState()` Hook

Students will learn:

- What is a Hook → built-in utility for adding React features
- `useState()` → to handle dynamic data inside components

Syntax fundamentals:

- State variable
- Setter function
- Initial value

Example activities:

- Simple **counter**
- Button click → change message (e.g., “Subscribed!”)
- Toggle visibility text (show/hide)

👉 State makes UI **interactive** without touching DOM manually

---

### 🎯 Expected Outcome of Session 2

By the end, students can:

✔ Create a Vite-based React project
✔ Understand all important files & folders
✔ Write/Render JSX components
✔ Explain why JSX is easier than DOM manipulation
✔ Understand necessity of state
✔ Use `useState()` for interactivity

---
