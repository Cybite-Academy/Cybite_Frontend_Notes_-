Awesome! Here's a set of **practice questions** on **JavaScript Objects**, thoughtfully structured to include **Objective**, **Theoretical**, and **Practical** exercises while **integrating all the topics** you've taught so far.

<br>
<br>

## 🔹 **Objective Questions (MCQs and Fill in the Blanks)**

1. **Which of the following is a correct way to define an object in JavaScript?**  
   a) `let person = new Object();`  
   b) `let person = {};`  
   c) `let person = Object.create();`  
   d) Both a and b

2. **What is the output of `typeof {}` in JavaScript?**  
   a) `"array"`  
   b) `"object"`  
   c) `"function"`  
   d) `"undefined"`

3. **In JavaScript, object keys are always stored as:**  
   a) strings  
   b) numbers  
   c) booleans  
   d) symbols

4. **Fill in the blank:**  
   To access the value of a property using a variable key name, we use ______ notation.

5. **Which method can be used to get all the keys of an object?**  
   a) `Object.keys()`  
   b) `Object.values()`  
   c) `Object.entries()`  
   d) `Array.keys()`

6. **What is the correct syntax to add a method called `greet` to an object named `user`?**  
   a) `user.greet = function() {}`  
   b) `user = { greet: () => {} }`  
   c) `function greet() {}; user.greet = greet;`  
   d) All of the above

<br>
<br>

## 🔹 **Theoretical Questions**

1. **Explain the difference between dot notation and bracket notation when working with objects. Provide examples.**

2. **Compare Arrays and Objects in JavaScript. When should you use one over the other?**

3. **Why are objects useful when dealing with real-world data in JavaScript applications?**

4. **How does the `typeof` operator help when working with objects and other data types?**

5. **Briefly describe what happens when you assign a function to a property inside an object.**

<br>
<br>

## 🔹 **Practical Exercises**

### Exercise 1: Create a Student Object  
Create an object called `student` that contains the following properties:
- `name` (string)
- `age` (number)
- `isEnrolled` (boolean)
- `courses` (array of course names)

Then:
- Add a method called `greet` that logs `"Hello, my name is [name]"`.
- Log the number of courses using array and object methods.

### Exercise 2: Dynamic Property Access  
Write a function `getPropValue(obj, key)` that returns the value of the given key in an object.  
Test it using:
```js
const book = { title: "Atomic Habits", author: "James Clear", pages: 320 };
console.log(getPropValue(book, "author")); // Should print "James Clear"
```

### Exercise 3: Using Loops with Objects  
Write a function that takes an object and prints all key-value pairs using a `for...in` loop.

### Exercise 4: Object Calculator  
Create an object `calculator` with methods:
- `add(a, b)`
- `subtract(a, b)`
- `multiply(a, b)`
- `divide(a, b)`

Each method should return the result of the operation.

Use it to:
```js
console.log(calculator.add(5, 3)); // 8
```

### Exercise 5: Integrating Arrays and Objects  
Create an array of student objects. Each object should have `name`, `score`, and a method `hasPassed()` that returns `true` if `score >= 50`.

Then:
- Use a loop to display which students passed.
- Use array methods to filter only students who passed.

### Bonus Practice (Advanced Integration):
- Use `Math.random()` and `Math.floor()` to randomly assign a score to each student.
- Create a function that receives a student object and returns a string summary like:  
  `"John scored 67. Passed: true"`

