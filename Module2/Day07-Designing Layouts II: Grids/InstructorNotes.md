# Designing Layouts II: Grids

### Part A: Session Flow / Topics to be Covered

**1. Introduction to CSS Grid** (15 minutes)

- Why Grid Layout? Problems with floats, Flexbox limitations for 2D layouts
- When to use Grid vs Flexbox
- Grid terminology: grid container, grid item, grid line, grid track, grid cell, grid area

**2. Creating a Grid Container** (15 minutes)

- `display: grid` vs `display: inline-grid`
- Defining rows and columns

  - `grid-template-rows`, `grid-template-columns`
  - Shorthand: `grid-template: rows / columns`

- Gap properties: `row-gap`, `column-gap`, `gap`

**3. Placing Grid Items** (20 minutes)

- Explicit vs implicit placement
- `grid-column` / `grid-row` start and end
- `grid-column-start`, `grid-column-end`, `grid-row-start`, `grid-row-end`
- `grid-area` for spanning multiple rows/columns

**4. Grid Track Sizing and Repeat Function** (15 minutes)

- Units: `px`, `%`, `fr`, `auto`
- Using `repeat()` function for repetitive tracks
- Example variations with fixed, flexible, and mixed tracks

**5. Grid Template Areas** (15 minutes)

- Defining named areas
- Assigning grid items to areas
- Advantages of template areas for layout readability

**6. Aligning Items in Grid** (15 minutes)

- `justify-items` → alignment along row (inline axis)
- `align-items` → alignment along column (block axis)
- `justify-content` → alignment of the entire grid along row
- `align-content` → alignment of the entire grid along column

**7. Responsive Grids and Auto-Fill / Auto-Fit** (15 minutes)

- Using `minmax()` for responsive columns
- `auto-fill` vs `auto-fit` behavior
- Media queries with grids

**8. Combining Grid with Box Model & Flexbox** (10 minutes)

- Practical use cases: nested grids, flexible layouts
- Integrating padding, margin, and borders inside grid items

**9. Hands-on Activity** (20 minutes)

- Build a dashboard/grid layout: cards, headers, footers, and content sections
- Experiment with spanning, gaps, alignment, and responsive behavior

---

### Part B: Detailed Notes / Content

---

#### **1. Introduction to CSS Grid**

**Why CSS Grid?**

- Traditional layouts using floats, inline-blocks, or even Flexbox have limitations for **2D layouts** (both rows and columns).
- CSS Grid is **designed specifically for 2D layouts**. It simplifies complex arrangements like dashboards, galleries, and magazine-style layouts.
- Grid allows **precise placement of items**, spacing control, and responsive layouts.

**Terminology:**

- **Grid Container** → element with `display: grid` or `display: inline-grid`
- **Grid Item** → direct child of grid container
- **Grid Line** → dividing line between tracks
- **Grid Track** → a row or column
- **Grid Cell** → intersection of a row and column
- **Grid Area** → a rectangular space formed by multiple cells

---

#### **2. Creating a Grid Container**

**Enable Grid on a container:**

```css
.container {
  display: grid; /* block-level grid */
  display: inline-grid; /* inline-level grid */
}
```

**Defining rows and columns:**

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px 1fr; /* three columns */
  grid-template-rows: 50px auto 100px; /* three rows */
}
```

**Shorthand for rows/columns together:**

```css
grid-template: 50px auto 100px / 100px 200px 1fr;
```

**Gaps between rows and columns:**

```css
.container {
  gap: 10px; /* shorthand for row & column */
  row-gap: 15px; /* only row gap */
  column-gap: 20px; /* only column gap */
}
```

---

#### **3. Placing Grid Items**

**Explicit placement:**

- `grid-column-start`, `grid-column-end`
- `grid-row-start`, `grid-row-end`

**Shorthand:**

```css
.item {
  grid-column: 1 / 3; /* starts at column 1, ends before column 3 */
  grid-row: 2 / 4; /* starts at row 2, ends before row 4 */
}
```

**Grid area placement:**

```css
.item {
  grid-area: 1 / 2 / 3 / 4; /* row-start / column-start / row-end / column-end */
}
```

**Implicit placement:**

- Items automatically fill empty grid cells if no explicit placement is given.

---

#### **4. Grid Track Sizing and Repeat Function**

**Units for grid tracks:**

- Fixed: `px`, `em`
- Percentage: `%`
- Flexible: `fr` (fraction of available space)
- Auto: `auto` (size according to content)

**Example with different units:**

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 100px auto;
}
```

**Repeat function:**

```css
grid-template-columns: repeat(3, 1fr); /* three equal columns */
grid-template-rows: repeat(2, 100px); /* two rows of 100px */
```

**Mixing repeat and explicit values:**

```css
grid-template-columns: repeat(2, 1fr) 200px 1fr;
```

---

#### **5. Grid Template Areas**

**Named areas simplify layout readability:**

```css
.container {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar content content"
    "footer footer footer";
  grid-template-columns: 150px 1fr 1fr;
  grid-template-rows: 60px 1fr 40px;
}
```

**Assign items to areas:**

```css
.header {
  grid-area: header;
}
.sidebar {
  grid-area: sidebar;
}
.content {
  grid-area: content;
}
.footer {
  grid-area: footer;
}
```

**Advantages:**

- Easier to visualize and maintain layout
- Works well for dashboard, magazine, or complex UI

---

#### **6. Aligning Items in Grid**

**Single item alignment inside its grid cell:**

- `justify-self` → horizontal alignment (start, end, center, stretch)
- `align-self` → vertical alignment (start, end, center, stretch)

**Container alignment of items:**

- `justify-items` → horizontal alignment of all items in their cells
- `align-items` → vertical alignment of all items in their cells

**Aligning the entire grid inside container:**

- `justify-content` → aligns grid along row (inline axis)
- `align-content` → aligns grid along column (block axis)

**Example:**

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 100px);
  grid-template-rows: repeat(2, 100px);
  justify-items: center;
  align-items: stretch;
  justify-content: space-between;
  align-content: center;
}
```

---

#### **7. Responsive Grids and Auto-Fill / Auto-Fit**

**Responsive columns with minmax():**

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 10px;
}
```

**Difference between auto-fill and auto-fit:**

- `auto-fill` → fills grid with as many tracks as possible, leaves empty tracks if space available
- `auto-fit` → stretches tracks to fill available space if fewer items

**Media Queries for responsiveness:**

```css
@media (max-width: 600px) {
  .container {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

---

#### **8. Combining Grid with Box Model & Flexbox**

- Grid items still obey **padding, margin, and border** rules from Box Model
- Can **nest Flexbox inside Grid items** for more control
- `margin: auto` works inside Grid items to center elements horizontally or vertically

**Example of nested Grid + Flexbox:**

```html
<div class="grid-container">
  <div class="card">
    <div class="flex-content">
      <div>Item 1</div>
      <div>Item 2</div>
    </div>
  </div>
</div>
```

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}
.card {
  border: 2px solid #ccc;
  padding: 10px;
}
.flex-content {
  display: flex;
  justify-content: space-between;
}
```

---

#### **9. Hands-on Activity (20 mins)**

- Create a **dashboard layout**: header, sidebar, content area, footer
- Include **grid gaps, spanning items, responsive behavior**
- Nest a **Flexbox inside grid items** for card layout or nav links
- Encourage testing all alignment properties (`justify-items`, `align-items`, `justify-content`, `align-content`)

---
