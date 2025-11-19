# **Making Webpages Interactive: DOM II — Rendering, Sorting & Filtering**

## **Learning Objectives**

* DOM traversal
* Create elements dynamically
* Append/appendChild difference
* Render data into table and cards
* Remove/replace nodes
* Sorting data & re-rendering
* Filtering data & re-rendering

---

### **DOM Traversal**

Teach with nested boxes.

#### Important properties:

* `parentElement`
* `children`
* `firstElementChild`
* `lastElementChild`
* `nextElementSibling`
* `previousElementSibling`
* `.closest()`

---

### **Creating & Appending DOM Elements**

Explain purpose: build UI dynamically.

#### **A. createElement**

```js
const div = document.createElement("div");
```

#### **B. appendChild (older method)**

* Always adds at the end
* Accepts only Node

```js
container.appendChild(div);
```

#### **C. append (modern)**

* Can append **Nodes + text**
* Can append **multiple items at once**

```js
container.append("Hello", div);
```

#### **D. innerHTML (quick but less safe)**

Use only when content is simple.

---

### **Appending Data into a Table (Dynamic Table Rendering)**

### Example:

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

Teach:

* Clearing table before re-render
* Creating rows dynamically
* Injecting data into table

---

### **Appending Data as Cards inside a Container**

### Example:

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

Teach:

* Creating card structure
* Using appendChild
* Styling cards via classes

---

### **Sorting Data + Re-Rendering into Table/Card**

Use `.sort()` then call render function again.

### Example: Sort by Name (A → Z)

```js
function sortByName() {
  data.sort((a, b) => a.name.localeCompare(b.name));
  renderTable(data);
  // or renderCards(data);
}
```

### Example: Sort by Number

```js
data.sort((a, b) => a.age - b.age);
renderTable(data);
```

Teach:

* Sorting array
* Clearing UI
* Re-appending sorted data

---

### **Filtering Data + Re-Rendering**

Use search input.

```js
function filterData(value) {
  const filtered = data.filter(item =>
    item.name.toLowerCase().includes(value.toLowerCase())
  );

  renderTable(filtered);
  // or renderCards(filtered);
}
```

Teach:

* filter() method
* Case insensitive search
* Updating UI live

---

### Removing Elements(Overview)

```js
row.remove();
card.remove();
```

---

