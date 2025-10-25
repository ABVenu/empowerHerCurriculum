# Styling with Precision: CSS Selectors & Combinators

### Part A: Session Flow/Learning Objectives 

1. **Demerits of Inline Styling** (10 minutes)

   * Discuss why inline styles are discouraged in larger projects.
   * Challenges with maintenance, reusability, and specificity conflicts.

2. **Introduction to CSS Selectors** (10 minutes)

   * Definition and purpose of selectors.
   * How selectors target elements for styling.

3. **Types of Selectors with Examples** (25 minutes)

   * **Universal selector (`*`)** – Example: `* { margin: 0; }`
   * **Type/Element selector** – Example: `p { color: blue; }`
   * **Class selector** – Example: `.highlight { background-color: yellow; }`
   * **ID selector** – Example: `#main-title { font-size: 24px; }`
   * **Group selector** – Example: `h1, h2, h3 { font-family: Arial; }`
   * **Attribute selector** – Example: `[type="text"] { border: 1px solid gray; }`

4. **Combinators in CSS** (25 minutes)

   * **Descendant combinator (`space`)** – Example: `div p { color: green; }`
   * **Child combinator (`>`)** – Example: `ul > li { list-style: square; }`
   * **Adjacent sibling combinator (`+`)** – Example: `h1 + p { margin-top: 0; }`
   * **General sibling combinator (`~`)** – Example: `h2 ~ p { color: gray; }`

5. **Specificity in CSS** (20 minutes)

   * Explain how CSS decides which rule to apply when multiple rules match the same element.
   * Specificity hierarchy: Inline > ID > Class/Attribute/Pseudo-class > Type > Universal.
   * Example:

     ```css
     #title { color: red; }       /* ID selector */
     .title { color: blue; }      /* Class selector */
     h1 { color: green; }         /* Type selector */
     ```
   * Show how the browser chooses `red` for an element with `id="title"` and `class="title"`.

6. **Hands-on Activity: Styling Using Selectors & Combinators** (20 minutes)

   * Students will create a small webpage with multiple nested elements.
   * Apply styles using different types of selectors and combinators.
   * Experiment with specificity to see which rules take precedence.

---

### Part B: Notes/Content

### **Overview**

* **Duration**: 1 hour 50 minutes
* **Objective**: Teach students to efficiently target HTML elements using CSS selectors and combinators, understand specificity, and highlight why inline styling is discouraged in favor of reusable styles.

### **Session Flow**

1. **Demerits of Inline Styling** (10 minutes)

   * Inline styles are hard to maintain and update across multiple elements.
   * They increase redundancy and reduce reusability.
   * Example: Updating the color of 20 paragraphs individually is cumbersome with inline styles.

2. **Introduction to CSS Selectors** (10 minutes)

   * CSS selectors define which HTML elements to style.
   * They are the foundation of structured, reusable CSS.

3. **Types of Selectors with Examples** (25 minutes)

   * **Universal Selector (`*`)**: Targets all elements.

     ```css
     * { margin: 0; padding: 0; }
     ```
   * **Type Selector**: Targets elements by tag name.

     ```css
     p { color: blue; }
     ```
   * **Class Selector**: Targets elements by class.

     ```css
     .highlight { background-color: yellow; }
     ```
   * **ID Selector**: Targets element by ID (unique).

     ```css
     #main-title { font-size: 24px; }
     ```
   * **Group Selector**: Targets multiple elements.

     ```css
     h1, h2, h3 { font-family: Arial; }
     ```
   * **Attribute Selector**: Targets elements with specific attributes.

     ```css
     [type="text"] { border: 1px solid gray; }
     ```

4. **Combinators in CSS** (25 minutes)

   * **Descendant**: Styles all elements inside a parent.

     ```css
     div p { color: green; }
     ```
   * **Child**: Styles direct children only.

     ```css
     ul > li { list-style: square; }
     ```
   * **Adjacent Sibling**: Styles the immediate next sibling.

     ```css
     h1 + p { margin-top: 0; }
     ```
   * **General Sibling**: Styles all following siblings.

     ```css
     h2 ~ p { color: gray; }
     ```

5. **Specificity in CSS** (20 minutes)

   * **Hierarchy**: Inline > ID > Class/Attribute/Pseudo-class > Type > Universal.
   * Demonstrate rule conflicts and how specificity resolves them.
   * Example:

     ```css
     #title { color: red; }       
     .title { color: blue; }      
     h1 { color: green; }         
     ```

     * Browser applies `red` because ID has higher specificity.

6. **Hands-on Activity** (20 minutes)

   * Build a webpage with nested elements (`div`, `ul`, `li`, `p`, etc.).
   * Apply styles using:

     * Various selectors (type, class, ID, attribute)
     * Combinators (descendant, child, sibling)
     * Observe specificity in action
   * Encourage experimentation and discussion about best practices.

---

