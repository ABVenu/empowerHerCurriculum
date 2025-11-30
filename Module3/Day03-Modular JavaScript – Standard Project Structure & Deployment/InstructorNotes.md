### Lecture Name

## Modular JavaScript – Standard Project Structure & Deployment

---

## Learning Objectives

By the end of this session, students will be able to:

- Explain what JavaScript modules are and why they are used.
- Create reusable files using ES6 `export` and `import`.
- Organize files in a professional project folder structure.
- Use modules to connect UI components across pages.
- Deploy a complete frontend project using a static hosting service.

---

## 1. Introduction to Modular JavaScript

As projects grow larger, keeping all code inside one HTML or JS file becomes difficult to manage.

To improve code readability and maintenance:

- Break the app into **small logical files**
- Each file handles **one specific responsibility**
- Then connect files using **imports & exports**

This approach is called **Modular JavaScript**.

---

## 2. ES6 Modules — Export & Import

ES6 introduced a native module system in JavaScript.
We can now write code in **separate files** and share functions, variables, or classes between them.

---

### 2.1 Named Exports

Use **named exports** when exporting multiple items.

**math.js**

```js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
```

**app.js**

```js
import { add, subtract } from "./math.js";

console.log(add(10, 5));
console.log(subtract(10, 5));
```

> Note: Imported names must match the exported names exactly.

---

### 2.2 Default Export

Each file can have **only one default export** → Ideal for the main function of the file.

**utils.js**

```js
export default function multiply(a, b) {
  return a * b;
}
```

**app.js**

```js
import multiply from "./utils.js";

console.log(multiply(4, 3));
```

---

### 2.3 Combining Default + Named Exports

**math.js**

```js
export default function divide(a, b) {
  return a / b;
}

export const pi = 3.14;
```

**app.js**

```js
import divide, { pi } from "./math.js";

console.log(divide(10, 2));
console.log(pi);
```

---

### Important Rule for Modules in Browser

When using modules in HTML:

- The script must be loaded with `type="module"`
- Use correct file path and include `.js` extension

Example:

```html
<script type="module" src="./app.js"></script>
```

---

## 3. Example: Reusable Navbar Module

### Step 1: Create a navbar module

**scripts/navbar.js**

```js
export function renderNavbar() {
  return `
    <nav>
      <a href="index.html">Home</a>
      <a href="login.html">Login</a>
      <a href="signup.html">Signup</a>
    </nav>
  `;
}
```

### Step 2: Import and render the navbar in multiple pages

**scripts/app.js**

```js
import { renderNavbar } from "./navbar.js";

document.getElementById("navbar").innerHTML = renderNavbar();
```

### Step 3: Add placeholder container in HTML

```html
<div id="navbar"></div>
<script type="module" src="./scripts/app.js"></script>
```

This prevents code duplication and improves maintainability.

---

## 4. **Standard Project Structure for Frontend DOM Applications**

A clean and consistent project structure is essential for:

- Better readability
- Easier collaboration in teams
- Smooth deployment to hosting platforms (like GitHub Pages, Netlify, Firebase Hosting)
- Faster debugging and maintenance
- Industry-level development practices

---

## Recommended Project Structure

```
project-folder/
│
├── index.html              → Main homepage (must be at root level)
│
├── pages/                  → All internal pages
│   ├── login.html
│   └── signup.html
│
├── scripts/                → All JavaScript files
│   ├── app.js
│   ├── login.js
│   ├── signup.js
│   └── auth.js
│
├── styles/                 → All CSS files
│   └── style.css
│
├── assets/                 → All images, icons, and other static files
│   └── images/
│
└── README.md               → Documentation for project
```

---

## Why should **index.html** always be at the root level?

- Hosting services look for `index.html` in the **root** to load your website.
- It is automatically treated as the **entry point** of the project.
- If the index page is placed inside a folder like `/pages/index.html`, the website may not open properly after deployment.

### Example of Deployment Issue

If index.html is not at root:

```
404 Not Found – No default page detected
```

### Correct behavior:

When index.html is at root:

```
https://username.github.io/project-folder/
→ Automatically opens index.html
```

So, index.html must always remain in the **top level of the project**.

---

## Benefits of Organized Folder Structure

| Folder    | Purpose                                  | Benefit                                       |
| --------- | ---------------------------------------- | --------------------------------------------- |
| pages     | Other UI pages like login, signup, about | Keeps root clean and organized                |
| scripts   | JS logic separated into modules          | Better maintainability & reusability          |
| styles    | All CSS styles                           | Easy styling management                       |
| assets    | Images, icons, fonts, PDFs               | Faster access and separation of static assets |
| README.md | Documentation                            | Helps others understand the project quickly   |

---

## What to Avoid

| Bad Practice                 | Example                                 | Problem                             |
| ---------------------------- | --------------------------------------- | ----------------------------------- |
| All files dumped in root     | index.html, app.js, login.html...       | Hard to navigate                    |
| HTML files in scripts folder | login.html in `/scripts/`               | Unprofessional structure            |
| Absolute file paths          | `/Users/Desktop/project/scripts/app.js` | Breaks after deployment             |
| No README file               | Lack of clarity & no setup instructions | Difficult for others to run project |

---

## Rules to Remember

- Always keep your main landing/home screen named as:

  ```
  index.html
  ```

- Place it in the root folder (not inside pages/)
- Use **relative paths** for linking files:

  - Example:

    ```html
    <script type="module" src="./scripts/app.js"></script>
    ```

- Organize and separate:

  - HTML → pages folder
  - CSS → styles folder
  - JS → scripts folder
  - Images → assets folder

---

## 5. Deployment Basics

After project completion, we must **deploy** the website so others can access it online.

Popular free static hosting platforms:

| Platform         | Type                            |
| ---------------- | ------------------------------- |
| GitHub Pages     | Upload using GitHub             |
| Netlify          | Drag-and-drop or Git deployment |
| Firebase Hosting | Part of Firebase platform       |

Deployment workflow:

1. Finalize project structure (no absolute paths)
2. Push project to GitHub or prepare build folder
3. Deploy to hosting service
4. Final testing in production environment

---

## 6. Key Takeaways

- Modular coding helps manage large applications easily.
- ES6 Modules allow splitting code into reusable files.
- Always use `<script type="module">` for imports in browsers.
- Maintain a clean and professional project structure.
- Deploy web apps to make them publicly accessible.

---
