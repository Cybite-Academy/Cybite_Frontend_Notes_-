Here’s a thoughtfully structured **set of practice questions on JavaScript Variables**, aligned with the topics you've taught so far. The questions are grouped into **Objective**, **Theoretical**, and **Practical** sections for balanced learning.

---

## 🧠 **Objective Questions (Multiple Choice & True/False)**  
Focus: Concept recall & identification

1. **Which keyword was introduced in ES6 for declaring block-scoped variables?**  
   A. `var`  
   B. `let`  
   C. `const`  
   D. `variable`

2. **What will be the output of `typeof "123"`?**  
   A. `number`  
   B. `string`  
   C. `boolean`  
   D. `undefined`

3. **Which of the following is a valid variable name?**  
   A. `2name`  
   B. `my-name`  
   C. `_value`  
   D. `class`

4. **True or False:**  
   Variables declared with `var` are function-scoped.

5. **Which data type does the value `true` belong to?**  
   A. String  
   B. Number  
   C. Boolean  
   D. Object

6. **What will `typeof undefined` return?**  
   A. `"null"`  
   B. `"undefined"`  
   C. `"object"`  
   D. `"NaN"`

7. **Which keyword should you use to declare a variable that will never be reassigned?**  
   A. `let`  
   B. `const`  
   C. `var`  
   D. `final`

---

## 📘 **Theoretical Questions**  
Focus: Explanation, definitions, comparisons

1. **Explain the differences between `var`, `let`, and `const`. Include use cases for each.**

2. **What is the `typeof` operator used for? List 3 examples with different data types.**

3. **Why should you avoid using `var` in modern JavaScript? Provide a scenario that could cause issues.**

4. **Describe how JavaScript handles variable hoisting with `var`, `let`, and `const`.**

5. **What is a data type in JavaScript? Name and describe the 3 primitive data types you've learned so far.**

6. **Can a variable declared with `const` hold an object? If yes, can you change the properties of that object? Explain with an example.**

---

## 🛠️ **Practical Exercises**  
Focus: Implementation and hands-on coding

### 🟠 Beginner Level
1. **Declare variables to store:**
   - Your name (as a string)
   - Your age (as a number)
   - Whether you are a student (as a boolean)

2. **Use `typeof` to log the type of each variable in the above question to the console.**

3. **Try reassigning values to variables declared with `var`, `let`, and `const`. Observe what happens. Write a short comment about your observation.**

---

### 🔵 Intermediate Level
4. **Create a script that calculates the area of a rectangle.**  
   - Declare two variables `length` and `width`  
   - Multiply them to get the area  
   - Log the result using a descriptive message

5. **Write a short program to swap the values of two variables.**  
   - Before: `a = 5`, `b = 10`  
   - After: `a = 10`, `b = 5`

6. **Use `typeof` inside an `if` condition to check if a variable is a string. If it is, convert it to uppercase and log it.**

---

### 🔴 Bonus Challenge
7. **Build a mini data checker:**
   - Declare 3 variables: `username`, `age`, and `isRegistered`
   - Check the types of each using `typeof`
   - If any is not of the correct type (`string`, `number`, `boolean`), log a message saying “Wrong data type for [variable]”

8. **Create a script that prints a message like:**
   ```javascript
   const name = "Jane";
   const age = 25;
   console.log(`Hi, my name is ${name} and I am ${age} years old.`);
   ```
   - Then try changing `name` and `age` to new values using `let` and print again.

