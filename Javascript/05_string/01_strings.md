# String

### **What is a String?**

A **string** is a **sequence of characters** (letters, numbers, symbols) used to store and manipulate text in programming. It is always written inside **quotes** (`" "` or `' '`).

Think of a string as **a sentence or a word inside a box** that a program can use.

---

### **Scenarios Where Strings are Used**

1. **Storing Names & Messages or Any Text Data.**
   - Example: `"John Doe"`, `"Hello, how are you?"`
2. **User Input in Forms**
   - Example: A website asks for your name and saves it as a string:
     ```jsx
     let userName = "Alice";
     console.log("Welcome, " + userName);
     ```
3. **Displaying Messages on a Website**
   - Example: `"Error! Please enter a valid email."`
4. **Concatenating (Joining) Strings**
   - Example:
     ```jsx
     let firstName = "John";
     let lastName = "Doe";
     let fullName = firstName + " " + lastName;
     console.log(fullName); // Output: John Doe
     ```
5. **Extracting & Searching Text**
   - Example: Checking if a word is in a sentence
     ```jsx
     let sentence = "JavaScript is fun!";
     console.log(sentence.includes("fun")); // Output: true
     ```
6. **Modifying & Formatting Text**
   - Example: Changing `"hello"` to uppercase
     ```jsx
     let text = "hello";
     console.log(text.toUpperCase()); // Output: HELLO
     ```

### **Key Points About Strings**

- Strings **must** be inside `""` or `''`.
- You can **join**, **modify**, **search**, and **format** strings.
- Strings are used **everywhere** in programming!
