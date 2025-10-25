# Let’s Style Web Blocks: Adding Colors, Fonts, Borders

### Part A: Session Flow/Learning Objectives 

1. **Introduction to Styling in HTML** (10 minutes)  
   - Overview of styling methods (inline, internal).
   - Advantages and use cases for inline and internal styles.

2. **Inline Styling** (15 minutes)  
   - Syntax and usage of inline styles.
   - Example: Applying styles to individual elements (color, font size, etc.).

3. **Internal Styling with `<style>` Tag** (20 minutes)  
   - Using internal styles in the `<head>` section.
   - Example: Applying styles for multiple elements within the document.

4. **Adding Background Colors** (15 minutes)  
   - Using different color formats (hexadecimal, RGB, named colors).
   - Example: Applying background colors to blocks and elements.

5. **Changing Font Properties** (15 minutes)  
   - Modifying font-size, font-family, and font-weight.
   - Example: Styling text with different fonts and sizes.

6. **Adding Text Colors** (10 minutes)  
   - Applying color to text elements using various methods.

7. **Styling Borders: Width, Color, and Style** (20 minutes)  
   - Controlling border width, color, and style (dotted, dashed, solid).
   - Example: Adding borders to divs, images, and text blocks.

8. **Hands-on Activity: Styling a Web Block** (15 minutes)  
   - Students will create a simple block with styled colors, fonts, and borders using inline and internal styles.

---
Got it! I’ll add **some realistic variations/examples** for background, fonts, text colors, and borders in **Part B**, while keeping **margin/padding** simple and without variations. Here’s the updated **Part B**:

---

### Part B: Notes/Content 

### **Overview**

* **Duration**: 1 hour 50 minutes to 2 hours 
* **Objective**: Introduce students to various styling techniques in HTML using inline styles and internal CSS. Emphasize the importance of colors, fonts, borders, and spacing (margin and padding) in web design.

### **Session Flow**

1. **Introduction to Styling in HTML** (10 minutes)

   * Discuss the significance of styling in enhancing user experience and improving readability.
   * Explain the difference between content structure and visual appearance.

2. **Inline Styling** (15 minutes)

   * **Explanation**: Inline styles apply CSS directly within an HTML element using the `style` attribute. Good for quick fixes but not recommended for larger projects.
   * **Example**:

     ```html
     <h1 style="color: blue; font-size: 24px; margin: 10px; padding: 5px;">Welcome to My Website</h1>
     ```
   * Encourage students to use inline styles sparingly.

3. **Internal Styling with `<style>` Tag** (15 minutes)

   * **Explanation**: Internal styles allow centralized control of multiple elements within the same document, improving organization.
   * **Example**:

     ```html
     <style>
       h1 {
         color: green;
         font-family: Arial, sans-serif;
         margin: 15px;
         padding: 10px;
       }
     </style>
     ```
   * Discuss when to use internal styles versus external styles.

4. **Adding Background Colors** (15 minutes)

   * **Explanation**: Background colors make elements visually distinct. Can be applied to blocks, headers, sections, or entire pages.
   * **Example Variations**:

     ```html
     <div style="background-color: lightblue; padding: 10px; margin: 10px;">Light blue block</div>
     <div style="background-color: #ffcccc; padding: 10px; margin: 10px;">Hex color example</div>
     <div style="background-color: rgb(200, 255, 200); padding: 10px; margin: 10px;">RGB color example</div>
     ```

5. **Changing Font Properties** (15 minutes)

   * **Explanation**: Font properties influence readability and style. You can change font-size, font-weight, font-family, and style.
   * **Example Variations**:

     ```html
     <p style="font-size: 18px; font-weight: bold; margin: 8px; padding: 5px;">Bold paragraph example</p>
     <p style="font-size: 16px; font-style: italic; font-family: 'Courier New'; margin: 8px; padding: 5px;">Italic Courier text</p>
     <p style="font-size: 20px; font-weight: 300; font-family: Verdana; margin: 8px; padding: 5px;">Light-weight Verdana text</p>
     ```

6. **Adding Text Colors** (10 minutes)

   * **Explanation**: Text color can highlight or emphasize content. Choose colors with enough contrast for readability.
   * **Example Variations**:

     ```html
     <span style="color: red; margin: 5px; padding: 2px;">Important text</span>
     <span style="color: green; margin: 5px; padding: 2px;">Success message</span>
     <span style="color: orange; margin: 5px; padding: 2px;">Warning message</span>
     ```

7. **Styling Borders: Width, Color, Style** (15 minutes)

   * **Explanation**: Borders help define sections and improve layout clarity. Common styles include **solid, dotted, dashed**, but you can also explore **double, groove, ridge, inset, outset**.
   * **Example Variations**:

     ```html
     <div style="border: 2px solid black; padding: 10px; margin: 10px;">Solid border</div>
     <div style="border: 2px dotted blue; padding: 10px; margin: 10px;">Dotted border</div>
     <div style="border: 2px dashed green; padding: 10px; margin: 10px;">Dashed border</div>
     <div style="border: 4px double purple; padding: 10px; margin: 10px;">Double border</div>
     <div style="border: 3px groove orange; padding: 10px; margin: 10px;">Groove border</div>
     ```

8. **Hands-on Activity** (10 minutes)

   * Assign students to create a styled block using:

     * Background colors (different formats)
     * Fonts (size, weight, style, family)
     * Text colors
     * Borders (with different styles)
     * Margin and padding for proper spacing
   * Encourage experimentation and creativity.

---


