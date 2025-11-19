# **Making Webpages Interactive: DOM I — Foundations & Element Manipulation**

## **Learning Objectives**

- Understand what the DOM is and why it exists
- Learn how browsers convert HTML → DOM Tree
- Access and select elements
- Change content, styles, and attributes dynamically

---

## **What is DOM?**

- DOM = Document Object Model
- Browser creates a **tree structure** from HTML
- JS can **read / modify / delete / add** elements in DOM
- DOM is not HTML — it is an **object structure** in memory

Use simple diagram:

```
Window
 └── Document
      └── html
            ├── head
            └── body
```

---

## **DOM Tree & Nodes**

- Node Types:

  - Element Node
  - Text Node
  - Comment Node
  - Document Node

---

## **DOM Selection Methods**

### **A. Modern & Preferred**

- `document.querySelector()`
- `document.querySelectorAll()`

### **B. Older Methods**

- `document.getElementById()`
- `document.getElementsByClassName()`
- `document.getElementsByTagName()`

👉 _Explain NodeList vs HTMLCollection._

---

## **DOM Manipulation – Basics**

- `.innerText` / `.textContent` / `.innerHTML`
- `.style` → Modify CSS
- `.setAttribute()` / `.getAttribute()`
- `.classList.add()` / `.remove()` / `.toggle()`

---

## **Live Working Example**

**HTML**

```html
<h2 id="title">Hello</h2>
<button id="btn">Change Text</button>
```

**JS**

```js
const title = document.querySelector("#title");
const btn = document.querySelector("#btn");

btn.addEventListener("click", function () {
  title.innerText = "Text Updated!";
  title.style.color = "blue";
});
```

Teach:

- Selecting elements
- Adding event listeners
- Modifying text/style

---
