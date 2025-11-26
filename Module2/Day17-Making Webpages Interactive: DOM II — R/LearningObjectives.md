
# **Making Webpages Interactive: DOM II — Rendering, Sorting & Filtering**

## **Learning Objectives**

* DOM traversal
* Create elements dynamically
* Append/appendChild differences
* Render data into table and cards
* Remove/replace nodes
* Sorting data & re-rendering
* Filtering data & re-rendering
* Navigating from one page to another

---

### **DOM Traversal**

Teach with nested boxes to visualize parent-child relationships.

#### Important Properties:

* `parentElement`
* `children`
* `firstElementChild`
* `lastElementChild`
* `nextElementSibling`
* `previousElementSibling`
* `.closest(selector)`

---

### **Creating & Appending DOM Elements**

Dynamic UI building in JavaScript.

#### **A. document.createElement()**

```js
const div = document.createElement("div");
```

#### **B. appendChild (older method)**

* Adds only Node elements
* Inserts at the end

```js
container.appendChild(div);
```

#### **C. append (modern)**

* Can add **text + multiple items**

```js
container.append("Hello", div);
```

#### **D. innerHTML**

* Quick but less safe (XSS risk)
* Re-renders entire content

---

## **Rendering Data into Table (Dynamic Rendering)**

```js
const data = [
  { name: "Sanidhya", age: 28 },
  { name: "Sukruth", age: 22 }
];

const tbody = document.querySelector("tbody");

function renderTable(arr) {
  tbody.innerHTML = "";

  arr.forEach(item => {
    const tr = document.createElement("tr");
    tr.innerHTML = `
      <td>${item.name}</td>
      <td>${item.age}</td>
    `;
    tbody.appendChild(tr);
  });
}

renderTable(data);
```

Concepts covered:
✔ Clear table before render
✔ Dynamically add rows
✔ Insert data inside HTML

---

## **Rendering Data as Cards**

```js
const container = document.querySelector("#cardContainer");

function renderCards(arr) {
  container.innerHTML = "";

  arr.forEach(item => {
    const card = document.createElement("div");
    card.className = "card";

    card.innerHTML = `
      <h3>${item.name}</h3>
      <p>Age: ${item.age}</p>
    `;
    container.appendChild(card);
  });
}

renderCards(data);
```

Concepts covered:
✔ Card structure
✔ appendChild
✔ Styling using class

---

## **Sorting Data + Re-Rendering**

### Sort by Name (A → Z)

```js
function sortByName() {
  data.sort((a, b) => a.name.localeCompare(b.name));
  renderTable(data);
}
```

### Sort by Number

```js
data.sort((a, b) => a.age - b.age);
renderTable(data);
```

✔ Update state
✔ Refresh UI using render function

---

## **Filtering Data + Re-Rendering**

```js
function filterData(value) {
  const filtered = data.filter(item =>
    item.name.toLowerCase().includes(value.toLowerCase())
  );

  renderTable(filtered);
}
```

✔ Live search
✔ Case-insensitive filter
✔ Shows only matching rows/cards

---

## **Removing Elements**

```js
row.remove();
card.remove();
```

✔ Remove any DOM node directly

---

## **Navigation — Moving from One Page to Another**

Use when a button or action should redirect the user.

### **window.location.href**

→ Loads a new webpage

```js
function goToNextPage() {
  window.location.href = "nextpage.html";
}
```

Other useful navigation properties:

* `window.location.assign("page.html")` → Adds to history
* `window.location.replace("page.html")` → Replaces current page (no back)

Example using button:

```html
<button onclick="window.location.href='contact.html'">Go to Contact</button>
```

✔ Useful for buttons, login flow, etc.

---

