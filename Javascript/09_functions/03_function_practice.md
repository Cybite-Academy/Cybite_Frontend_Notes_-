Here are practice questions on **Functions** in JavaScript, covering **objective, theoretical, and practical exercises** while integrating the topics you've been taught so far.

---

## **1. Objective Questions**

- **Question 1:** How do you correctly define a function in JavaScript?

  - a) `function myFunction { console.log("Hello"); }`
  - b) `function myFunction() { console.log("Hello"); }`
  - c) `def myFunction() { console.log("Hello"); }`
  - d) `func myFunction() { console.log("Hello"); }`

- **Question 2:** What will the following code output?

  ```javascript
  function greet(name) {
    return "Hello, " + name;
  }
  console.log(greet("John"));
  ```

  - a) `Hello,`
  - b) `Hello, John`
  - c) `John`
  - d) `undefined`

- **Question 3:** Which keyword is used to return a value from a function?

  - a) `return`
  - b) `output`
  - c) `print`
  - d) `console.log`

- **Question 4:** What will happen if a function is called without the required parameters?

  ```javascript
  function add(a, b) {
    return a + b;
  }
  console.log(add(5));
  ```

  - a) `5`
  - b) `undefined`
  - c) `NaN`
  - d) `error`

- **Question 5:** What is an arrow function in JavaScript?
  - a) A function defined using `=>` syntax
  - b) A function that can only return numbers
  - c) A function that runs only once
  - d) A function inside an object

---

## **2. Theoretical Questions**

- **Question 1:** What is the difference between a function declaration and a function expression? Provide an example of each.

- **Question 2:** Explain the concept of parameters and arguments in JavaScript functions with examples.

- **Question 3:** How does JavaScript handle default parameter values? Provide an example of a function with a default parameter.

- **Question 4:** What is an **anonymous function** in JavaScript? How does it differ from a named function?

- **Question 5:** Describe the difference between a **regular function** and an **arrow function** in JavaScript.

---

## **3. Practical Exercises**

- **Exercise 1:** Write a function named `sumNumbers` that takes two numbers as arguments and returns their sum.

- **Exercise 2:** Create a function called `isEven` that takes a number and returns `true` if it is even, and `false` otherwise.

- **Exercise 3:** Write a function that takes a string as input and returns the length of the string.

- **Exercise 4:** Define an arrow function named `multiplyByTwo` that takes a number as input and returns the number multiplied by 2.

- **Exercise 5:** Write a function called `greetUser` that takes a username as a parameter and logs `"Hello, [username]!"` to the console. If no username is provided, it should default to `"Guest"`.

- **Exercise 6:** Create a function `getRandomNumber` that generates a random number between 1 and 100 using JavaScript's `Math` methods.

- **Exercise 7:** Write a function `convertToUpperCase` that takes a string and returns the string in uppercase.

- **Exercise 8:** Write a function called `reverseString` that takes a string and returns the reversed version of it.

---

## **4. Bonus Questions**

- **Question 1:** What will be the output of the following code?

  ```javascript
  function testScope() {
    let x = 10;
    if (true) {
      let x = 20;
      console.log(x);
    }
    console.log(x);
  }
  testScope();
  ```

  - a) `10 20`
  - b) `20 10`
  - c) `20 20`
  - d) `10 10`

- **Question 2:** Modify the `sumNumbers` function so that it can take any number of arguments and return their sum.

- **Question 3:** What happens if a function does not have a `return` statement? Demonstrate this with an example.
