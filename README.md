# Instructor Guide: Intro to CSS

## **Learning Objectives**
By the end of this module, students will be able to:
1. Set up a basic CSS development environment.
2. Understand the structure and syntax of a CSS rule.
3. Apply the CSS box model to manage layout and spacing.
4. Use common CSS properties to style HTML elements effectively.
5. Differentiate and use element, ID, class, and combinator selectors.
6. Organize styles using multiple stylesheets.
7. Leverage CSS variables for maintainable and scalable styling.

---

## **Lesson Plan**

### **Setup (5 min)**
- Navigate to the project directory and create the required `index.html` and `style.css` files.
- Use Emmet to add boilerplate HTML, linking the CSS file within the `<head>`.
- Open the file in a browser for live preview.

**Activity:**
- Guide students to set up their development environment and create the project structure.

---

### **Concepts (2 min)**
- Overview of CSS: What it is and its purpose.
    - CSS controls a web page's layout, colors, fonts, and other visual aspects.
- Analogy: CSS is like decorating a house, where HTML provides the structure.
- Explain the separation of content (HTML) and presentation (CSS).
    - CSS enables us to separate a document's structure & content (HTML) from its presentation (CSS).
  
**Activity:**
- Demonstrate adding a simple CSS rule to change the text color of an `<h1>` tag to blue.

---

### **CSS Fundamentals (10 min)**
- ✨ **Diagram - [discuss syntax](https://raw.git.generalassemb.ly/modular-curriculum-all-courses/intro-to-css/main/fundamentals/assets/css-syntax.png?token=AAALP5NLYRS2YUVL4DXX5NTHRTD44):** Break down a CSS rule (selector, property, value).
    - **1)** Selectors: Used to target the element(s) to be styled and range from simple to incredibly complex.
    - **2)** Properties are written in lower-kebab-case
    - **3)** Value: The valid values that can be applied to a property are specific to that property.
    - **4)** Declaration: The combination of a property and value, separated by a colon and ending with a semi-colon, makes a declaration.
    - **5)** Rule: A selector and all of its associated declarations.
- ✨ **Selectors:** CSS element selectors target every instance of a specific HTML element
- ✨ **Comments:** Show how to add single-line and multi-line comments.
- ```css
  p {
  color: purple; /*All p elements will now have purple text!*/
    }
  ```

**🧑‍💻 Activity:**
- Add CSS to change text color, font size, and text alignment for an `<h1>` element.

**🙋‍♀️ Student Picker Questions:**
<details>
<summary>What are the components of a CSS rule?</summary>
Selector, property, and value.
</details>
<details>
<summary>How do you add a comment in CSS?</summary>
Use `/* comment */`.
</details>

---

### **Box Model (15 min)**
- ✨ Explain the four parts of the box model: content, padding, border, margin.
- ✨ **Diagram - [Everything is a box](https://git.generalassemb.ly/modular-curriculum-all-courses/intro-to-css/blob/main/box-model/assets/box-model.png):** Visualize the box model and its impact on layout.
- ✨ Demonstrate padding, border, and margin properties.

**🧑‍💻 Activity:**
- Style a `<div>` to explore padding, border, and margin effects.

**🙋‍♀️ Student Picker Questions:**
<details>
<summary>What is padding?</summary>
The space between content and the border of an element.
</details>
<details>
<summary>What is margin?</summary>
The space between the border of an element and adjacent elements.
</details>

---

### **Common Properties (10 min)**
- ✨ Font properties: `font-family`, `font-size`, `font-style`, `text-align`.
- ✨ Color properties: Hex, RGB, and named colors.
- ✨ Background colors and text styling.

**🧑‍💻 Activity:**
- Style text with font and color properties.
- Experiment with `background-color` and `text-align`.

**🙋‍♀️ Student Picker Questions:**
<details>
<summary>What are the three ways to specify a color in CSS?</summary>
Hex, RGB, and color names.
</details>
<details>
<summary>What does `font-family` do?</summary>
Specifies the font for the text.
</details>

---

### **Selectors (10 min)**
- ✨ Explain element, ID, and class selectors.
- ✨ Demonstrate combinator selectors (e.g., descendant selector).

**🧑‍💻 Activity:**
- Use class and ID selectors to style specific elements.
- Experiment with descendant selectors.

**🙋‍♀️ Student Picker Questions:**
<details>
<summary>How do you target an element with a specific ID?</summary>
Use `#id` in CSS.
</details>
<details>
<summary>What is the difference between class and ID selectors?</summary>
Class selectors can be reused; ID selectors must be unique.
</details>

---

### **Multiple Stylesheets (5 min)**
- ✨ Discuss the benefits of organizing CSS into multiple files.
- ✨ Explain the order of precedence when loading stylesheets.

**🧑‍💻 Activity:**
- Add a second stylesheet to handle specific styles and observe precedence.

**🙋‍♀️ Student Picker Questions:**
<details>
<summary>Why might you use multiple stylesheets?</summary>
For organization and easier maintenance.
</details>
<details>
<summary>Which stylesheet has higher precedence?</summary>
The one listed later in the HTML `<head>`.
</details>

---

### **CSS Variables (10 min)**
- ✨ Define and use CSS variables.
- ✨ Explain inheritance and reusability with variables.

**🧑‍💻 Activity:**
- Define a `--primary-color` variable and use it across multiple rules.
- Update the variable to observe changes.

**🙋‍♀️ Student Picker Questions:**
<details>
<summary>How do you define a CSS variable?</summary>
Use `--variable-name: value;`.
</details>
<details>
<summary>How do you use a CSS variable?</summary>
Use `var(--variable-name)`.
</details>

---

### **Level-Up Content**
#### **Shorthand Properties (5 min)**
- ✨ Demonstrate shorthand for padding, margin, and border.

#### **History of CSS (5 min)**
- ✨ Brief overview of CSS evolution and its impact on web development.

**Activity:**
- Research the history of CSS or experiment with shorthand properties.

---

### **Resources**
1. [MDN CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
2. [CSS Tricks](https://css-tricks.com/)
3. [Emmet Cheatsheet](emmet-cheatsheet.md)

---

### **Total Estimated Time:** 75 minutes
