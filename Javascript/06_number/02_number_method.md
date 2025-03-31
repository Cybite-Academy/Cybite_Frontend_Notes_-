# **Number Methods**

Number methods help in performing operations on numeric values.

### **Common Number Methods & Use Cases:**

| Method | Use Case | Example |
| --- | --- | --- |
| `.toFixed(n)` | Round number to `n` decimal places | `(3.14159).toFixed(2)` → `"3.14"` |
| `.toString()` | Convert number to string | `(100).toString()` → `"100"` |
| `Math.round(n)` | Round to nearest whole number | `Math.round(4.6)` → `5` |
| `Math.floor(n)` | Round down | `Math.floor(4.9)` → `4` |
| `Math.ceil(n)` | Round up | `Math.ceil(4.1)` → `5` |

### **Example Pseudo Code in JavaScript:**

```jsx
javascript
CopyEdit
let number = 5.678;
console.log(number.toFixed(2));  // Output: 5.68
console.log((100).toString());   // Output: "100"
console.log(Math.round(4.6));    // Output: 5
console.log(Math.floor(4.9));    // Output: 4
console.log(Math.ceil(4.1));     // Output: 5

```