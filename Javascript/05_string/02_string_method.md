# **String Methods**

String methods allow us to manipulate and work with text.

### **Common String Methods & Use Cases:**

| Method                   | Use Case                  | Example                                 |
| ------------------------ | ------------------------- | --------------------------------------- |
| `.length`                | Get string length         | `"Hello".length` → `5`                  |
| `.toUpperCase()`         | Convert text to uppercase | `"hello".toUpperCase()` → `"HELLO"`     |
| `.toLowerCase()`         | Convert text to lowercase | `"WORLD".toLowerCase()` → `"world"`     |
| `.slice(start, end)`     | Extract part of a string  | `"Hello".slice(0, 3)` → `"Hel"`         |
| `.replace("old", "new")` | Replace text in a string  | `"Hello".replace("H", "J")` → `"Jello"` |

### **Example Code:**

```jsx
let greeting = "Hello, World!";
console.log(greeting.length); // Output: 13
console.log(greeting.toUpperCase()); // Output: HELLO, WORLD!
console.log(greeting.replace("World", "Alice")); // Output: Hello, Alice!
```
