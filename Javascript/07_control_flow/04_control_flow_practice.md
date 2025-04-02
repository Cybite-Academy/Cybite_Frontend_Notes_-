Here are some simple practice questions on control flow, focusing on the topics you've taught so far:

### **1. Objective Questions**
- **Question 1:** Which of the following is the correct syntax for an `if` statement in JavaScript?
  - a) `if x > 5 { console.log(x); }`
  - b) `if (x > 5) { console.log(x); }`
  - c) `if x > 5 then { console.log(x); }`
  - d) `if x > 5: { console.log(x); }`

- **Question 2:** What will the following code print to the console?
  ```javascript
  let x = 10;
  if (x > 5) {
    console.log("Greater than 5");
  } else {
    console.log("Less than or equal to 5");
  }
  ```
  - a) `Greater than 5`
  - b) `Less than or equal to 5`
  - c) `undefined`
  - d) `error`

- **Question 3:** Which of the following is the correct syntax for a `for` loop in JavaScript?
  - a) `for (let i = 0; i < 5; i++) { console.log(i); }`
  - b) `for (let i = 0, i < 5, i++) { console.log(i); }`
  - c) `for i = 0; i < 5; i++ { console.log(i); }`
  - d) `for (let i = 0 to 5) { console.log(i); }`

- **Question 4:** What is the output of this code?
  ```javascript
  let x = 3;
  switch (x) {
    case 1:
      console.log("One");
      break;
    case 2:
      console.log("Two");
      break;
    default:
      console.log("Other");
  }
  ```
  - a) `One`
  - b) `Two`
  - c) `Other`
  - d) `undefined`

### **2. Theoretical Questions**
- **Question 1:** Explain the difference between `if` and `switch` statements in JavaScript. When would you choose to use one over the other?

- **Question 2:** What is the `else if` condition used for in JavaScript? How does it differ from the simple `else` statement?

- **Question 3:** What happens if there is no `break` statement in a `switch` block? Provide an example demonstrating this behavior.

- **Question 4:** How do the `&&` (AND) and `||` (OR) operators work in control flow conditions? Provide examples of both.

### **3. Practical Exercises**
- **Exercise 1:** Write a JavaScript program that takes a number as input and prints whether the number is even or odd using an `if-else` statement.

- **Exercise 2:** Using a `for` loop, print all the numbers from 1 to 10, inclusive, to the console.

- **Exercise 3:** Write a program that uses a `switch` statement to print the name of the day of the week based on a number (1 for Sunday, 2 for Monday, etc.). If the number is outside the range of 1 to 7, print `"Invalid day"`.

- **Exercise 4:** Write a program that checks if a string is "hello" using an `if` statement. If it is, print `"Hello, World!"`; otherwise, print `"Goodbye!"`.

- **Exercise 5:** Create a program that uses a `while` loop to sum all numbers from 1 to a given number `n`. Log the result to the console.

### **4. Bonus Questions**
- **Question 1:** Given the following code, what will be the output?
  ```javascript
  let x = 20;
  if (x > 10 && x < 30) {
    console.log("Between 10 and 30");
  } else {
    console.log("Outside the range");
  }
  ```

- **Question 2:** Write a program that uses an `if-else` chain to check a person's age and print their life stage. For example, if the age is less than 12, print `"Child"`, if the age is between 12 and 19, print `"Teenager"`, and if the age is 20 or above, print `"Adult"`.

