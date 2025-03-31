# JavaScript Variables - Explained Simply

In JavaScript, **variables** are used to store and manage data. Think of them as labeled containers that hold values.

---

<br>

### Pseudo code

```jsx
let yourVariableName = datatypeValue;
```

<br>
<br>

## **1. Declaring Variables**

JavaScript provides **three** ways to declare variables:

### **🔹 `var` (Old way, avoid using)**

```jsx
var name = "John";
console.log(name); // Output: John
```

- **Has function scope** (not block scope).
- Can be **redeclared** in the same scope.
- Avoid using `var` in modern JavaScript.

### **🔹 `let` (Modern way, recommended)**

```jsx
let age = 25;
console.log(age); // Output: 25
```

- **Block-scoped** (only accessible inside `{}` where it's declared).
- Can be **updated** but **not redeclared** in the same scope.

### **🔹 `const` (For fixed values)**

```jsx
const PI = 3.14;
console.log(PI); // Output: 3.14
```

- **Block-scoped** like `let`.
- **Cannot be reassigned** after declaration.
- Useful for constants (values that don’t change).

---

## **2. Variable Naming Rules**

✔ Can contain **letters, digits, `$`, and `_`**

✔ Must **start with a letter, `$`, or `_`** (not a number)

✔ Case-sensitive (`myVar` and `myvar` are different)

```jsx
let firstName = "Alice"; // ✅ Correct
let _score = 100;        // ✅ Correct
let $price = 50;         // ✅ Correct
let 1stPlace = "John";   // ❌ Error (Cannot start with a number)

```

---

## **3. Data Types in Variables**

JavaScript variables can hold different types of values.

### **🔹 String (Text)**

```jsx
let game = "Esports League";
console.log(typeof game); // Output: string
```

### **🔹 Number (Integer or Float)**

```jsx
let score = 99.5;
console.log(typeof score); // Output: number
```

### **🔹 Boolean (True/False)**

```jsx
let isWinner = true;
console.log(typeof isWinner); // Output: boolean
```

### **🔹 Undefined (No Value Assigned)**

```jsx
let player;
console.log(typeof player); // Output: undefined
```

### **🔹 Null (Intentional Empty Value)**

```jsx
let user = null;
console.log(typeof user); // Output: object (JS quirk, but it's null)
```

### **🔹 Object (Key-Value Pairs)**

```jsx
let playerStats = { name: "John", score: 1500 };
console.log(typeof playerStats); // Output: object
```

### **🔹 Array (List of Values)**

```jsx
let scores = [100, 200, 300];
console.log(typeof scores); // Output: object (Arrays are objects)
```

### **🔹 Function (A Block of Code)**

```jsx
function greet() {
  return "Hello!";
}
console.log(typeof greet); // Output: function
```

---

## **4. Variable Scope**

### **🔹 Global Scope (Accessible Everywhere)**

```jsx
var globalVar = "I am global";

function test() {
  console.log(globalVar); // Accessible
}
test();
console.log(globalVar); // Also accessible
```

### **🔹 Block Scope (Only Inside `{}`)**

```jsx
if (true) {
  let blockVar = "I exist only here";
  console.log(blockVar); // ✅ Works inside the block
}
console.log(blockVar); // ❌ Error (blockVar is not defined)
```

---

## **5. Use Case Scenarios**

### **🔹 Tracking Player Scores in a Game**

```jsx
let playerName = "Alice";
let score = 0;

score += 10; // Player earns points
console.log(`${playerName} scored: ${score}`);
```

### **🔹 Checking User Login Status**

```jsx
let isLoggedIn = true;

if (isLoggedIn) {
  console.log("Welcome back!");
} else {
  console.log("Please log in.");
}
```

### **🔹 Storing User Profile Data**

```jsx
const userProfile = {
  name: "John",
  age: 30,
  isPremium: true,
};

console.log(userProfile.name); // Output: John
```

### **🔹 Counting Down in a Timer**

```jsx
let countdown = 5;

const timer = setInterval(() => {
  console.log(`Time left: ${countdown} seconds`);
  countdown--;

  if (countdown < 0) {
    clearInterval(timer);
    console.log("Time's up!");
  }
}, 1000);
```

---

### **Summary**

| **Keyword** | **Reassignment?** | **Redeclaration?** | **Scope** |
| ----------- | ----------------- | ------------------ | --------- |
| `var`       | ✅ Yes            | ✅ Yes             | Function  |
| `let`       | ✅ Yes            | ❌ No              | Block     |
| `const`     | ❌ No             | ❌ No              | Block     |

### **💡 Best Practices**

✔ Use `let` for variables that might change.

✔ Use `const` for values that shouldn't change.

✔ Avoid `var` (outdated and may cause bugs).
