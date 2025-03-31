# Number

In **JavaScript**, numbers are a **primitive data type** used for performing mathematical operations, storing values, and handling calculations. JavaScript only has one type of number (`Number`), which can be **integers, decimals (floating point), or special values like `Infinity` and `NaN`**.

---

### **1. Declaring Numbers**

```jsx
let num1 = 10; // Integer
let num2 = 3.14; // Floating-point number (decimal)
let num3 = -5; // Negative integer
```

---

### **2. Basic Math Operations**

```jsx
let a = 10;
let b = 4;

console.log(a + b); // Addition → 14
console.log(a - b); // Subtraction → 6
console.log(a * b); // Multiplication → 40
console.log(a / b); // Division → 2.5
console.log(a % b); // Modulus (Remainder) → 2
console.log(a ** 2); // Exponentiation → 100 (10^2)
```

---

### **3. Special Number Values**

```jsx
console.log(10 / 0); // Infinity
console.log(-10 / 0); // -Infinity
console.log("hello" * 5); // NaN (Not a Number)
```

---

### **4. Working with Decimal Numbers**

JavaScript uses floating-point precision, which can cause small errors:

```jsx
console.log(0.1 + 0.2); // 0.30000000000000004 (not exactly 0.3)

console.log((0.1 + 0.2).toFixed(2)); // "0.30" (fix precision)
```

---

### **5. Number Methods**

JavaScript provides methods for working with numbers:

```jsx
let num = 123.456;

console.log(num.toFixed(2)); // "123.46" (rounds to 2 decimal places)
console.log(num.toPrecision(4)); // "123.5" (limits significant digits)
console.log(Number.isInteger(10)); // true (checks if number is an integer)
console.log(Number.isNaN("hello" * 5)); // true (checks if value is NaN)
console.log(Number.parseInt("42px")); // 42 (converts string to integer)
console.log(Number.parseFloat("3.14em")); // 3.14 (converts string to float)
```

---

### **6. Use Case Scenarios**

### **a) Validating User Input (e.g., Age Input)**

```jsx
function validateAge(input) {
  let age = Number.parseInt(input);
  if (Number.isNaN(age) || age <= 0) {
    console.log("Invalid age");
  } else {
    console.log("Valid age:", age);
  }
}

validateAge("25"); // Valid age: 25
validateAge("abc"); // Invalid age
```

### **b) Generating Random Numbers (e.g., Dice Roll)**

```jsx
let diceRoll = Math.floor(Math.random() * 6) + 1;
console.log("You rolled:", diceRoll);
```

### **c) Formatting Currency (e.g., Price Display)**

```jsx
let price = 1999.99;
console.log(
  price.toLocaleString("en-US", { style: "currency", currency: "USD" })
);
// Output: "$1,999.99"
```

### **d) Countdown Timer (e.g., Tournament Start)**

```jsx
let timeLeft = 10;

let countdown = setInterval(() => {
  console.log(`Time left: ${timeLeft} seconds`);
  timeLeft--;

  if (timeLeft < 0) {
    clearInterval(countdown);
    console.log("Tournament Started!");
  }
}, 1000);
```

---

JavaScript numbers are **versatile and easy to use** but require careful handling due to floating-point precision issues. 🚀
