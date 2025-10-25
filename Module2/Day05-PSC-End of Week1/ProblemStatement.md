### Solve a typcial problem which comprises of all the learnings of HTML/CSS

## **Problem Statement: Build a “Student Profile Dashboard”**

**Objective:** Create a fully structured, styled, and interactive HTML page showcasing a student profile dashboard. This will test HTML, CSS, and CSS selectors/combinators knowledge.

---

### **Requirements**

#### 1. **HTML Structure (Sessions 1–2)**

* Create a main container `<div>` with `id="dashboard"`.
* Add a header `<header>` with the title: **“Student Profile Dashboard”**.
* Include a navigation menu `<nav>` with at least 3 links (Home, Profile, Contact).
* Create a **profile section** `<section>` with:

  * Student Name (`<h2>`), Age (`<p>`), and a short Bio (`<p>`).
* Include a **table** `<table>` showing the student’s subjects and marks. At least 4 rows (Subject, Marks, Grade).
* Add a **form** `<form>` to update student info:

  * Fields: Name (text), Age (number), Bio (textarea), Favorite Subject (select dropdown).
  * Include a submit button.

---

#### 2. **Styling (Session 3)**

* Use **internal CSS** for styling (avoid inline styles unless necessary).
* Style the **header** with background color, font color, and padding.
* Style the **table** with borders, alternating row colors, and readable fonts.
* Style the **form** elements: input boxes, textarea, and dropdown. Add border-radius and hover effect on submit button.
* Use colors and fonts to make sections visually distinct.

---

#### 3. **Selectors & Combinators (Session 4)**

* Use **class selectors** to style repeated elements like paragraphs in the bio.
* Use **ID selectors** for unique elements like `#dashboard` and `#submit-btn`.
* Use **descendant combinators** to style nested elements, e.g., `section p` inside profile section.
* Use **child combinators** to style direct children of the table like `table > tr`.
* Use **adjacent sibling combinators** to style the paragraph immediately following a header.
* Use **general sibling combinators** to style all elements after the form inside the section.
* Demonstrate **specificity** by creating conflicting rules and showing which style applies (e.g., `.bio {color: gray;}` vs `#dashboard p {color: black;}`).

---

#### 4. **Hands-on/Bonus**

* Add a small **hover effect** on table rows and navigation links using combinators.
* Ensure the layout is neat and visually appealing.
* Add comments in HTML and CSS explaining which selectors and combinators are used where.

---

✅ **Expected Outcome**

* Students demonstrate knowledge of HTML structure, tables, forms, and semantic elements.
* Proper application of styling techniques and avoidance of inline styles.
* Correct use of CSS selectors, combinators, and specificity to style elements efficiently.
* Fully functional, visually distinct, and maintainable dashboard page.


