## Datatypes

In simple terms, a **data type** in JavaScript refers to the kind of value a variable can hold. Think of it as a way for JavaScript to understand what type of data you're working with.

### JavaScript has two main types of data:

1. **Primitive Data Types** (Basic types)

   - **Number** → `10`, `3.14`, `50`
   - **String** → `"Hello"`, `'JavaScript'`
   - **Boolean** → `true`, `false`
   - **Undefined** → A variable declared but not given a value (`let x;`)
   - **Null** → An intentional empty value (`let y = null;`)
   - **Symbol** → Unique identifiers (used in advanced cases)
   - **BigInt** → Large numbers beyond the `Number` limit (`1234567890123456789n`)

1. **Non-Primitive Data Types** (Complex types)
   - **Object** → A collection of key-value pairs (`{ name: "John", age: 25 }`)
   - **Array** → A list of values (`[1, 2, 3]`)
   - **Function** → A reusable block of code (`function greet() { console.log("Hi!"); }`)

In short, **data types tell JavaScript how to treat a value**—whether it's a number, text, or a more complex structure like an object. 🚀

### **Use Case Scenarios for Data Types in JavaScript**

1. **Numbers** (`Number`) → Used for mathematical calculations

   ```
   let price = 250;
   let discount = 20;
   let finalPrice = price - discount;
   console.log(finalPrice); // 230

   ```

   **Use Case**: Calculating prices in an e-commerce app.

2. **Strings** (`String`) → Used for storing and displaying text

   ```
   let username = "JohnDoe";
   console.log("Welcome, " + username + "!");

   ```

   **Use Case**: Displaying a user's name on a website.

3. **Booleans** (`true` / `false`) → Used for decision-making (if conditions)

   ```
   let isLoggedIn = true;
   if (isLoggedIn) {
       console.log("Show user dashboard");
   } else {
       console.log("Show login page");
   }

   ```

   **Use Case**: Checking if a user is logged in or not.

4. **Undefined** (`undefined`) → Used when a variable has been declared but not assigned a value

   ```
   let user;
   console.log(user); // undefined

   ```

   **Use Case**: Detecting uninitialized variables in a program.

5. **Null** (`null`) → Used to represent an empty or non-existent value

   ```
   let cart = null;
   console.log(cart); // null

   ```

   **Use Case**: Indicating that a shopping cart is empty in an e-commerce site.

6. **Objects** (`{}`) → Used to group related data together

   ```
   let user = {
       name: "Alice",
       age: 28,
       isMember: true
   };
   console.log(user.name); // Alice

   ```

   **Use Case**: Storing user profile details.

7. **Arrays** (`[]`) → Used for lists of data

   ```
   let scores = [85, 90, 78];
   console.log(scores[1]); // 90

   ```

   **Use Case**: Storing multiple scores in a quiz app.

8. **Functions** (`function`) → Used to execute a block of code

   ```
   function greet(name) {
       return "Hello, " + name + "!";
   }
   console.log(greet("John")); // Hello, John!

   ```

   **Use Case**: Creating reusable code for greeting users.

Each **data type** is used depending on what kind of information you need to store and how you want to process it! 🚀
