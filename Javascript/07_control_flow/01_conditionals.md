# Conditionals

### **Conditionals in JavaScript**

Conditionals are used to make decisions in code. They check whether a condition is **true** or **false** and then execute different code based on conditions.

---

### **1. if Statement** (Executes if the condition is true)

```jsx
let age = 18;

if (age >= 18) {
  console.log("You can vote!");
}
```

✔ If the condition is `true`, the block **executes**.

❌ If `false`, it **skips** to the next code.

✅ **Use Case**: Checking if a user is old enough to vote.

### **2. if...else Statement** (Runs one block if true, another if false)

```jsx
let isLoggedIn = false;

if (isLoggedIn) {
  console.log("Welcome back!");
} else {
  console.log("Please log in.");
}
```

✔ If the condition is **false**, the `else` block runs.

✅ **Use Case**: Checking if a user is logged in or not.

### **3. if...else if...else (Multiple conditions)**

```jsx
let score = 75;

if (score >= 90) {
  console.log("Grade: A");
} else if (score >= 80) {
  console.log("Grade: B");
} else if (score >= 70) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
```

✔ JavaScript **checks conditions one by one** until it finds a `true` case.

✔ If no conditions match, the `else` block runs.

✅ **Use Case**: Assigning grades based on a student's score.

### **4. Ternary Operator (`? :`)** (Shorter way to write an if...else)

```jsx
let isMember = true;
let discount = isMember ? "10% off" : "No discount";
console.log(discount);
```

✅ **Use Case**: Giving discounts to members.

### **5. switch Statement** (Checks multiple possible values and an Alternative to if-else)

```jsx
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Start of the week!");
    break;
  case "Friday":
    console.log("Weekend is near!");
    break;
  case "Sunday":
    console.log("Relax! It's the weekend!");
    break;
  default:
    console.log("Just another day.");
}
```

✔ `case` checks for **matching values**.

✔`break`**exits the switch** (if missing, the next case runs).
✔ `default` runs if **no case matches**.

✅ **Use Case**: Handling different actions based on the day of the week.

### **6. Logical Operators in Conditionals**

### `&&` (AND) → All conditions must be true

```jsx
let age = 20;
let hasID = true;

if (age >= 18 && hasID) {
  console.log("You can enter the club.");
}
```

✅ **Use Case**: Checking if a person is old enough AND has an ID.

### `||` (OR) → At least one condition must be true

```jsx
let hasKey = false;
let knowsPassword = true;

if (hasKey || knowsPassword) {
  console.log("You can enter the house.");
}
```

✅ **Use Case**: Checking if a person has a key OR knows the password.

### `!` (NOT) → Reverses a condition

```jsx
let isRaining = false;

if (!isRaining) {
  console.log("Go outside!");
}
```

✅ **Use Case**: Running code when it **is not** raining.

---

### **Summary**

- `if` → Runs if condition is true
- `if...else` → Runs one block if true, another if false
- `if...else if...else` → Handles multiple conditions
- `? :` (Ternary) → Short if...else
- `switch` → Handles multiple fixed values
- `&&`, `||`, `!` → Used for combining conditions

Conditionals help control the flow of a program by making **decisions** based on different situations! 🚀

### More Examples

### **✅ Checking User Access Level (if-else)**

```jsx
js;
CopyEdit;
let userRole = "admin";

if (userRole === "admin") {
  console.log("Access to all features");
} else if (userRole === "editor") {
  console.log("Access to editing features");
} else {
  console.log("Read-only access");
}
```

---

### **✅ Checking Payment Methods (Switch)**

```jsx
js;
CopyEdit;
let paymentMethod = "credit_card";

switch (paymentMethod) {
  case "cash":
    console.log("Pay with cash");
    break;
  case "credit_card":
    console.log("Pay with card");
    break;
  case "paypal":
    console.log("Pay with PayPal");
    break;
  default:
    console.log("Invalid payment method");
}
```
