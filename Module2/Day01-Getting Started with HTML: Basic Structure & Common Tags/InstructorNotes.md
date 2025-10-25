### Lecture Name

# Getting Started with HTML - Basic Structure & Common Tags

### Part A: Session Flow/Learning Objectives 

### **1. Introduction to HTML (10 mins)**

- What is HTML?
- Importance of HTML in web development.
- HTML’s role in structuring web pages and working with CSS and JavaScript.

---

### **2. HTML Document Structure (20 mins)**

- Anatomy of an HTML document:
  - `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`
  - Metadata: `<title>`, `<meta>`
- **Hands-on Activity**: Create a basic HTML page with title and body content.

---

### **3. Common HTML Tags (25 mins)**

- **Headings**: `<h1> to <h6>`
- **Paragraphs**: `<p>` and **line breaks**: `<br>`
- **Bold and Italic text**: `<b>`, `<i>`
- **Lists**: Ordered (`<ol>`) and unordered (`<ul>`) lists with `<li>` items.
- **Grouping Content**:
  - **`<div>`**: Block-level element for grouping multiple elements.
- **Hands-on Activity**:
  - Create a webpage with headings, paragraphs, lists, and a `<div>` to group content.

---

### **4. Images and Links (20 mins)**

- **Adding Images**: `<img src="..." alt="...">`
  - Importance of the `alt` attribute for accessibility.
- **Creating Links**: `<a href="...">`
  - Difference between internal and external links.
- **Hands-on Activity**:
  - Add an image and links to the page.

---

### **5. Commenting in HTML (10 mins)**

- **Purpose of Comments**:
  - Organizing code, adding notes, and disabling sections of code.
- **Syntax**:
  ```html
  <!-- This is a comment -->
  ```
- **Hands-on Activity**:
  - Add comments throughout the webpage to label sections and temporarily disable a code block.

---

### **6. Creating a Simple Web Page (25 mins)**

- **Task**: Build a webpage with the elements covered so far:
  - Headings, paragraphs, lists, images, links, and grouped sections using `<div>`.
- **Practice**:
  - Guide students to structure their webpage logically and preview it in a browser.

---

### **7. Recap and Q&A (5 mins)**

- **Summary of Key Topics**:
  - HTML structure, common tags, and the role of `<div>`.
  - Importance of comments for clear coding.
- **Open Floor for Questions**:
  - Address any doubts or issues raised by students.

---

### Part B: Instructor Notes/Content

---

### **1. Introduction to HTML (10 mins)**

- **HTML Overview:**

  - Explain that **HTML** stands for **HyperText Markup Language** and is the standard language for building web pages.
  - It defines the **structure of web content**, like headings, paragraphs, lists, links, and images.
  - Compare HTML to the **framework** of a building: Just as the building needs a structure, web pages need HTML to lay out content.

- **HTML’s Role in Web Development:**
  - HTML works together with **CSS (for styling)** and **JavaScript (for interactivity)**.
  - **Browsers render HTML** to display content according to the markup.

---

### **2. HTML Document Structure (20 mins)**

- **Walkthrough of Basic HTML Structure:**

  1. **`<!DOCTYPE html>`**:
     - Informs the browser that this is an HTML5 document.
  2. **`<html>`**:
     - The root element containing all other HTML elements.
  3. **`<head>`**:
     - Holds metadata about the webpage, like the title, character encoding, and links to stylesheets.
     - Example:
       ```html
       <head>
         <title>My First Web Page</title>
         <meta charset="UTF-8" />
       </head>
       ```
  4. **`<body>`**:
     - Contains all visible content that the browser renders, such as text, images, and links.

- **Hands-on Practice:**
  - Have students create a basic HTML page with the following code:
    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>My First HTML Page</title>
      </head>
      <body>
        <h1>Welcome to My Page!</h1>
        <p>This is a paragraph.</p>
      </body>
    </html>
    ```

---

### **3. Common HTML Tags (25 mins)**

- **Headings: `<h1>` to `<h6>`**
  - Headings are used to define section titles, with `<h1>` being the most important and `<h6>` the least.
  - Example:
    ```html
    <h1>Main Heading</h1>
    <h2>Subheading</h2>
    ```
- **Paragraphs: `<p>` and Line Breaks: `<br>`**

  - Use `<p>` to create a paragraph, and `<br>` to insert a line break.
  - Example:
    ```html
    <p>This is the first line.<br />This is the second line.</p>
    ```

- **Bold and Italic Text: `<b>` and `<i>`**

  - Use `<b>` for bold and `<i>` for italic text.
  - Example:
    ```html
    <p>This is <b>bold</b> and <i>italic</i> text.</p>
    ```

- **Lists: Unordered (`<ul>`) and Ordered (`<ol>`)**

  - **Unordered List (`<ul>`)** uses bullet points, while **Ordered List (`<ol>`)** uses numbers.
  - Example:
    ```html
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
    </ul>
    <ol>
      <li>Step 1</li>
      <li>Step 2</li>
    </ol>
    ```

- **Grouping Content with `<div>`**
  - Use `<div>` as a block-level element to group related content.
  - Example:
    ```html
    <div>
      <h2>About Me</h2>
      <p>I am a web development enthusiast.</p>
    </div>
    ```

---

### **4. Images and Links (20 mins)**

- **Adding Images:**

  - Use `<img>` to embed an image and include an `alt` attribute for accessibility.
  - Example:
    ```html
    <img src="https://example.com/image.jpg" alt="Sample Image" />
    ```

- **Creating Links:**

  - Use the `<a>` tag to create links to other web pages or sections within the same page.
  - Example:
    ```html
    <a href="https://www.example.com">Visit Example</a>
    ```

- **Hands-on Practice:**
  - Ask students to add an image and two links (one internal and one external) to their HTML page.

---

### **5. Creating a Simple Web Page (25 mins)**

- **Task Overview:**
  - Guide students to build a simple webpage that contains headings, paragraphs, lists, images, and links, and wrap related sections with `<div>` tags.
  - Encourage students to experiment with different heading levels and lists.

---

### **6. Commenting in HTML (10 mins)**

- **Purpose of Comments:**

  - Comments help organize code, add notes for developers, and temporarily disable sections of code.
  - They are ignored by browsers and do not appear on the webpage.

- **Syntax of Comments:**

  ```html
  <!-- This is a comment -->
  ```

- **Examples of Using Comments:**

  1. **Labeling sections:**

     ```html
     <!-- Header Section -->
     <h1>Welcome to My Webpage</h1>
     ```

  2. **Disabling code for testing:**

     ```html
     <!-- <p>This paragraph is hidden for now.</p> -->
     ```

  3. **Adding notes for future updates:**
     ```html
     <!-- TODO: Add a footer section -->
     ```

- **Activity:**
  - Ask students to add comments to each section of their HTML page.

---

### **7. Recap and Q&A (5 mins)**

- **Summary of Key Topics:**

  - The structure of an HTML document.
  - Common tags such as headings, paragraphs, lists, images, and links.
  - How to group elements with `<div>`.
  - The importance of using comments for clarity and collaboration.

- **Open Floor for Questions:**
  - Allow students to ask questions and clarify any doubts.

---
