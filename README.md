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
- ✨ **Diagram - [Everything is a box](https://git.generalassemb.ly/modular-curriculum-all-courses/intro-to-css/blob/main/box-model/assets/box-model.png):** Visualize the box model and its impact on layout.
- ✨ Explain the four parts of the box model: content, padding, border, margin.
- ✨ [Padding](https://git.generalassemb.ly/modular-curriculum-all-courses/intro-to-css/blob/main/box-model/assets/button.png) is the space between the content of an element and its border.
    - ```css
      p {
          /* all four sides */
          padding: 2px;
        }

      p {
          padding-bottom: 1px;
          padding-left: 2px;
          padding-right: 3px;
          padding-top: 4px;
        }
      ```

- ✨ Border - the area (typically a line) surrounding the padding. Borders are useful for separating elements from each other
    - ```css
      p {
          border: 3px solid red;
        }
      /* we could break this into three lines */
      p {
          border-width: 3px;
          border-style: solid;
          border-color: red;
        }
      ```
- ✨ Margin is the space between the border and other elements.
    - ```css
         p {
          /* all four sides */
          margin: 2px;
        }
      ```
    - `margin-top`, `margin-right`, and so on are also available.
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
CSS properties are used to control the appearance and behavior of HTML elements. There are many different CSS properties, but some of the most common ones are font properties, color, and background.

- ✨ Font properties: `font-family`, `font-size`, `font-weight`, `font-style`, `text-align`.
    - ```css
      h2 {
          font-family: Arial, sans-serif;
          font-size: 28px;
          font-weight: bold;
          font-style: italic;
          text-align: center;
        }
      ```

- ✨ Color properties: Hex (`#FF0000`), RGB `rgb(255, 0, 0)`, and named colors (`red`) - all 3 of those will give us the same color!
    - There are only [140 predefined color keywords](http://web.simmons.edu/~grovesd/comm244/notes/week3/css3-color-names) in CSS, but over 16 million possible hex/RGB color combinations exist.


**🎓 You Do (1):**
Take a few minutes and visit one of the following resources and learn more about a couple of properties of your choosing:

- [CSS-Tricks](https://css-tricks.com/almanac/properties/) - one of the best sites for all things CSS
- [codrops](https://tympanus.net/codrops/css_reference/#section_css-property)

After you've learned about that property, apply it in your code.

**🎓 You Do (2):**

Now that you've learned about some common properties, let's get some more practice.

- Set the margin on `<body>` element to 0 on all four sides. This is a common reset we do on all our pages because most browsers give a margin to the body element, which we usually do not want.
- Also, give the background of the `<body>` element a color of `lightgray`.
- Set the margin on the `<ul>` elements to 0 on all four sides.
- Set the text color of all `<div>` elements to `blue`.

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
    - ```css
      .important {
          color: red;
          font-weight: bold;
        }
      
      #about {
          font-style: italic;
          color: hotpink;
        }
      ```
- ✨ Demonstrate combinator selectors (e.g., descendant selector). The most common combinator is the descendant selector, but there are many more.

We use the descendant selector to target elements nested within another element, ***regardless of the depth of the nesting***. Note that this rule does not target `<div>` elements, only `<p>` elements. The last item in the combinator receives the styling.
    - ```css
    /* This will match all <p> tags nested anywhere within an <div> tag */
    div p { ... }
     ```
     
**🎓 You Do :**
Target the elements with the class name `super-cool`, and give them a border that is solid, 2px wide, and pink in color.

Note how the styling from both the `.important` and the `.super-cool` rules are applied to the div with both class names! What happens when you use conflicting declarations, like adding a `color: blue;` to the `.super-cool` rule?

Play around with the order of these rules in your CSS document, and try switching the order of the class names to `"super-cool important"` in the `div` element's `class` attribute. When is order important? When is it not? Explore these mechanics a bit on your own.

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
    - When creating larger projects - especially ones with multiple pages - our CSS can quickly get messy if we only use one stylesheet.
    - We can create a separate stylesheet for each page or section of our web app, allowing us to keep things tidy.
- To use multiple stylesheets, add a `<link>` element to the `<head>` section of your HTML code for each stylesheet that you want to use.
    - ```html
      <!DOCTYPE html>
        <html>
        <head>
          <link rel="stylesheet" href="global.css">
          <link rel="stylesheet" href="store-page.css">
        </head>
        <body>
          <!-- body content -->
        </body>
        </html>
      ```
- ✨ Explain the order of precedence when loading stylesheets.
    - When a browser loads multiple stylesheets for a web page, it will apply the styles in the order that the stylesheets are linked in the <head> section of the HTML code. This means that the styles in the later stylesheets will override the styles in the earlier stylesheets.

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
- Example CSS WITHOUT variables
    - ```css
      h1 {
          color: #7289DA;
        }
        
        a {
          background-color: #7289DA;
          color: #FFFFFF;
        }
        
        button {
          background-color: #7289DA;
          color: #FFFFFF;
        }
        
        #comments {
          border: 2px solid #7289DA;
        }
        
        footer {
          background-color: #7289DA;
          color: #FFFFFF;
        }
    ```
- Example CSS WITH variables
      - ```css
  
      /* MAKE VARIABLE */
          body {
          --brand-color: #7289DA;
        }
      /* USE IT */
        h1 {
          color: var(--brand-color);
        }
        
        a {
          background-color: var(--brand-color);
          color: #FFFFFF;
        }
        
        button {
          background-color: var(--brand-color);
          color: #FFFFFF;
        }
        
        #comments {
          border: 2px solid var(--brand-color);
        }
        
        footer {
          background-color: var(--brand-color);
          color: #FFFFFF;
        }
        ```

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
