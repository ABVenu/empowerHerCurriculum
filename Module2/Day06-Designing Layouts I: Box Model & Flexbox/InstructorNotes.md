
# Designing Layouts I: Box Model & Flexbox

---

### Part A: Session Flow / Learning Objectives

1. **Introduction to Box Model** (30 minutes)

   * What is the Box Model
   * Components: Content, Padding, Border, Margin
   * Box sizing (`content-box` vs `border-box`)
   * Padding properties and shorthand
   * Margin properties, shorthand, and `margin: auto`
   * Border properties: width, style, color, shorthand
   * Width and height calculations

2. **Introduction to Flexbox** (60 minutes)

   * Why Flexbox? Importance in modern web design
   * How Flexbox changes layout and responsiveness
   * Flex container properties: `display`, `flex-direction`, `flex-wrap`, `justify-content`, `align-items`, `align-content`
   * Flex item properties: `order`, `flex-grow`, `flex-shrink`, `flex-basis`, `align-self`
   * Combining Box Model with Flexbox for responsive layouts

3. **Hands-on Activity** (20 minutes)

   * Build layouts using Box Model + Flexbox
   * Experiment with spacing, alignment, and responsive arrangement

---

### Part B: Detailed Notes / Content (Complete Guide with Code)

#### **Box Model (30 mins)**

**Introduction:**

* Every HTML element is a rectangular **box**.
* Understanding Box Model is key for spacing, layout, and element sizing.

**Components of the Box Model:**

1. **Content:** Text or media inside the element.

2. **Padding:** Space between content and border.

   ```html
   <div style="padding: 20px; background-color: lightblue;">Padding Example</div>
   ```

   * Shorthand: `padding: 10px 20px 15px 5px;` → top right bottom left
   * `padding: 10px 20px;` → vertical | horizontal

3. **Border:** Surrounds padding and content.

   ```html
   <div style="border: 3px dashed green; padding: 10px;">Dashed Border</div>
   ```

   * Variations: `solid`, `dotted`, `dashed`, `double`, `groove`, `ridge`, `inset`, `outset`
   * Shorthand: `border: 2px solid red;`

4. **Margin:** Space outside the border.

   ```html
   <div style="margin: 20px; border: 2px solid black; padding: 10px;">Margin Example</div>
   ```

   * Shorthand: `margin: 10px 15px;` → vertical | horizontal
   * `margin: auto;` → horizontally center block elements

5. **Box sizing:**

   ```html
   <div style="width: 200px; padding: 20px; border: 5px solid blue; box-sizing: border-box;">
       Box Sizing Example
   </div>
   ```

   * `content-box` → width/height includes only content
   * `border-box` → width/height includes padding & border

**Width & Height Calculation:**

* Total width = content + padding + border + margin

---

#### **Flexbox (60 mins)**

**Introduction:**

* **Why Flexbox?** Traditional layouts using floats, inline-block, or positioning are limited and non-responsive.
* Flexbox simplifies alignment, spacing, and distribution **in one dimension (row or column)**.
* Works for **dynamic content, cards, navbars, grids**.

**Flex Container Properties:**

1. **display:**

   ```css
   display: flex; /* block-level flex container */
   display: inline-flex; /* inline-level flex container */
   ```

2. **flex-direction:**

   ```css
   flex-direction: row; /* left → right */
   flex-direction: row-reverse; /* right → left */
   flex-direction: column; /* top → bottom */
   flex-direction: column-reverse; /* bottom → top */
   ```

3. **flex-wrap:**

   ```css
   flex-wrap: nowrap; /* default, single line */
   flex-wrap: wrap; /* wrap items to next line */
   flex-wrap: wrap-reverse; /* wrap in reverse direction */
   ```

4. **justify-content:** (main axis alignment)

   ```css
   justify-content: flex-start;
   justify-content: flex-end;
   justify-content: center;
   justify-content: space-between;
   justify-content: space-around;
   justify-content: space-evenly;
   ```

5. **align-items:** (cross axis alignment, single line)

   ```css
   align-items: flex-start;
   align-items: flex-end;
   align-items: center;
   align-items: baseline;
   align-items: stretch; /* default */
   ```

6. **align-content:** (cross axis alignment, multi-line)

   ```css
   align-content: flex-start;
   align-content: flex-end;
   align-content: center;
   align-content: space-between;
   align-content: space-around;
   align-content: stretch; /* default */
   ```

---

**Flex Item Properties:**

1. **order:** change visual order

   ```css
   order: 1; /* default 0 */
   ```

2. **flex-grow:** proportion to grow in available space

   ```css
   flex-grow: 1; /* grow to fill space */
   ```

3. **flex-shrink:** proportion to shrink when space is limited

   ```css
   flex-shrink: 1; /* shrink if necessary */
   ```

4. **flex-basis:** initial size of item before growing/shrinking

   ```css
   flex-basis: 200px;
   ```

5. **align-self:** override container’s align-items for individual item

   ```css
   align-self: flex-start;
   align-self: center;
   align-self: stretch;
   ```

---

**Combining Box Model with Flexbox:**

* Padding, border, and margin still apply inside flex items.
* `margin: auto;` is powerful for centering flex items horizontally or vertically.
* Example:

```html
<div style="display: flex; justify-content: center; align-items: center; height: 200px; border: 2px solid gray;">
  <div style="padding: 20px; margin: auto; border: 2px solid blue;">Centered Item</div>
</div>
```

**Hands-on / Practical Tips:**

* Build navbars, card layouts, gallery grids using Flexbox.
* Experiment with all `justify-content`, `align-items`, `align-content` variations.
* Use `flex-grow`, `flex-shrink`, `flex-basis` to control responsiveness.
* Inspect in dev tools to visualize Box Model + Flex behavior.

---


