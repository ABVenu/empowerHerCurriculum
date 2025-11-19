# **Making Webpages Interactive: DOM II — Rendering, Sorting & Filtering**

## **Learning Objectives**

#### **1. Understand JSON as a Data Format**

* Explain what JSON is and why it's used in web applications
* Identify valid JSON structure (keys, values, arrays, objects)
* Understand the difference between **JavaScript Objects** and **JSON**
* Validate and format JSON using tools like JSONLint

---

#### **2. Convert Data Between JS Objects and JSON**

* Use `JSON.stringify()` to convert objects → JSON string
* Use `JSON.parse()` to convert JSON string → object
* Understand when and why parsing/stringifying is needed

---

#### **3. Store Data Persistently in Browser Storage**

* Understand what **Web Storage API** is
* Differentiate between **LocalStorage** and **SessionStorage**
* Know the limitations (5MB capacity, string-only storage, security concerns)

---

#### **4. Perform CRUD Operations on LocalStorage/SessionStorage**

* Save data (`setItem`)
* Retrieve data (`getItem`)
* Update stored data (modify JSON → stringify → save again)
* Delete specific data (`removeItem`)
* Clear all storage (`clear`)

---

#### **5. Store and Retrieve Arrays/Objects in Storage**

* Convert arrays/objects to JSON before storing
* Parse JSON back to JS objects when reading
* Render stored data into UI (e.g., table/cards)

---

#### **6. Use Storage for Real Web Application Use Cases**

* Save form data
* Remember user preferences
* Store last visited page, theme, or temporary session data
* Create simple persistent features (e.g., todo list, cart items)

---

#### **7. Handle Common Errors & Pitfalls**

* Understand storage only stores **strings**
* Handle parsing errors
* Avoid circular JSON structures
* Know when to use sessionStorage vs localStorage

---

