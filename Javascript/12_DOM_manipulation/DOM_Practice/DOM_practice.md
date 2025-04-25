Here’s a thoughtfully structured **set of practice questions** on **JavaScript DOM**, integrating all the topics you’ve taught so far. The questions are divided into **Objective**, **Theoretical**, and **Practical** sections to promote a well-rounded understanding and application.

---

## 🧠 **Objective Questions (Multiple Choice & True/False)**
Focus: Concept recall & identification

1. **Which of the following is not a valid JavaScript data type?**  
   A. String  
   B. Integer  
   C. Boolean  
   D. Object

2. **What will `typeof NaN` return?**  
   A. "undefined"  
   B. "number"  
   C. "NaN"  
   D. "object"

3. **Which method adds an item to the end of an array?**  
   A. `push()`  
   B. `shift()`  
   C. `unshift()`  
   D. `pop()`

4. **Which of the following will correctly access an HTML element with id `title`?**  
   A. `getElementById("title")`  
   B. `document.title`  
   C. `document.getElement("title")`  
   D. `document.getElementById("title")`

5. **True or False:**  
   `Math.floor(4.7)` will return `5`.

6. **Which of these is used to loop through object properties?**  
   A. `forEach`  
   B. `map()`  
   C. `for...in`  
   D. `for...of`

7. **Which method converts a string to uppercase?**  
   A. `toUpper()`  
   B. `upperCase()`  
   C. `toUpperCase()`  
   D. `uppercase()`

---

## 📘 **Theoretical Questions**
Focus: Explanation, comparison, and definitions

1. **Explain the difference between `var`, `let`, and `const` in variable declarations.**

2. **Differentiate between primitive and non-primitive data types in JavaScript, giving examples.**

3. **What is the purpose of the `typeof` operator? Provide three different examples and their outputs.**

4. **Describe what the Document Object Model (DOM) is in your own words. Why is it important in web development?**

5. **How do conditionals like `if-else` improve decision-making in JavaScript code? Provide an example involving a user's age.**

6. **Compare and contrast the `map()` and `forEach()` array methods. When should each be used?**

7. **What is the significance of `this` in object methods? Illustrate with an example.**

---

## 🛠️ **Practical Exercises**
Focus: Implementation and hands-on coding

### 🟠 Beginner DOM Practice
1. **Create a simple HTML file with a button. Write JavaScript that changes the button text to "Clicked!" when the button is clicked.**

2. **Write a script that takes input from a text field and displays it in a paragraph when a "Submit" button is clicked.**

3. **Create an array of 5 colors. On clicking a button, change the background color of the page to a random color from the array.**

---

### 🔵 Intermediate DOM Practice (with integration)
4. **Design a basic calculator with buttons for add, subtract, multiply, and divide. Take two number inputs and display the result using DOM methods.**

5. **Build a mini student list manager:**
   - Input: Student name
   - Button: Add to list
   - Output: Display in a list using `ul` and `li`
   - Bonus: Show total number of students using `length`

6. **Use object methods to dynamically update DOM content:**
   ```javascript
   const user = {
     name: "Ada",
     age: 22,
     greet: function() {
       return `Hello, I am ${this.name} and I am ${this.age} years old.`;
     }
   };
   ```
   - Display the `greet()` message in an HTML paragraph on page load.

---

### 🔴 Advanced Practical Challenge
7. **Build a simple to-do list app with the following:**
   - Input field to add task
   - Button to add
   - Display list of tasks
   - Button next to each task to "Remove"
   - Use array methods (`push`, `splice`) and DOM manipulation

8. **Create a random quote generator:**
   - Store 5 quotes in an array of objects (`{ quote, author }`)
   - On button click, show a random quote and author on screen
