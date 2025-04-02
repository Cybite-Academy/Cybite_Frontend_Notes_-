Here are simple practice questions on arrays and related topics that cover both theoretical and practical exercises based on what you've been taught so far:

### **1. Objective Questions**

- **Question 1:** Which of the following is a valid way to declare an array in JavaScript?

  - a) `let arr = [1, 2, 3];`
  - b) `let arr = (1, 2, 3);`
  - c) `let arr = {1, 2, 3};`
  - d) `let arr = 1, 2, 3;`

- **Question 2:** What is the output of the following code?

  ```javascript
  let arr = [10, 20, 30];
  console.log(arr.length);
  ```

  - a) `3`
  - b) `undefined`
  - c) `30`
  - d) `error`

- **Question 3:** Which of the following is the correct method to add an element to the end of an array?

  - a) `arr.push()`
  - b) `arr.pop()`
  - c) `arr.shift()`
  - d) `arr.unshift()`

- **Question 4:** What will be the result of the following expression?
  ```javascript
  let arr = [5, 10, 15];
  arr[1] = 20;
  console.log(arr);
  ```
  - a) `[5, 20, 15]`
  - b) `[5, 10, 15]`
  - c) `[20, 15]`
  - d) `error`

### **2. Theoretical Questions**

- **Question 1:** Explain what the `typeof` operator does in JavaScript and how it is used. Provide examples with arrays and other data types.

- **Question 2:** What is the difference between `let`, `const`, and `var` when declaring variables in JavaScript? How do they behave with arrays?

- **Question 3:** Describe how the `map()` and `filter()` methods work on arrays. Provide an example of each method in use.

- **Question 4:** What will happen if you try to access an index of an array that does not exist? For example:
  ```javascript
  let arr = [1, 2, 3];
  console.log(arr[5]);
  ```

### **3. Practical Exercises**

- **Exercise 1:** Create an array called `numbers` containing the integers from 1 to 5. Use the `push()` method to add the number 6 at the end of the array. Then, use `console.log()` to print the updated array.

- **Exercise 2:** Write a program that accepts a string array of names, converts each name to uppercase using the `map()` method, and then logs the new array.

- **Exercise 3:** Given the array `let arr = [3, 6, 9, 12]`, use the `filter()` method to create a new array containing only the even numbers.

- **Exercise 4:** Write a program that sums all the numbers in an array using the `reduce()` method. For example, given `let arr = [1, 2, 3, 4]`, the program should return `10`.

- **Exercise 5:** Using the array `let arr = ['apple', 'banana', 'cherry']`, write a program that finds the index of the element `'banana'` using the `indexOf()` method and logs it to the console.

### **4. Bonus Questions**

- **Question 1:** What will be the output of the following code snippet?
  ```javascript
  let arr = [1, 2, 3, 4, 5];
  console.log(arr.slice(1, 3));
  ```
- **Question 2:** Write a function `isArrayEmpty(arr)` that checks if an array is empty and returns `true` if it is, or `false` otherwise.
