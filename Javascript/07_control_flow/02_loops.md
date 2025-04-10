# Loops

Loops help us **repeat** a block of code multiple times **without writing it manually**.

---

### **1. for Loop** (Runs a code a set number of times)

Loops **repeat** code until a condition is false.

```jsx
for (let i = 1; i <= 5; i++) {
    console.log("Iteration " + i);
}

```

✔ Starts at `i = 1`, runs while `i <= 5`, and increases `i` by `1` each time.

✅ **Use Case**: Printing numbers from 1 to 5.

### **2. while Loop** (Runs **while** a condition is true)

```jsx
let count = 1;

while (count <= 5) {
    console.log("Count: " + count);
    count++;
}

```

✔ Useful when **you don’t know the number of repetitions** in advance.

✅ **Use Case**: Running code **until** a condition is false.

### **3. do...while Loop** (Runs **at least once**, then repeats while true)

```jsx
let num = 1;

do {
    console.log("Number: " + num);
    num++;
} while (num <= 5);

```

✔ Runs **at least once**, even if the condition is `false`.

✅ **Use Case**: Ensuring code runs **once** before checking a condition.

### **4. for...of Loop** (Loops through items in an **array**)

```jsx
let scores = [90, 85, 78, 92];

for (let score of scores) {
    console.log("Score: " + score);
}

```

✅ **Use Case**: Looping through a list of values.

### **5. for...in Loop** (Loops through properties in an **object**)

```jsx
let user = { name: "Alice", age: 25, country: "Nigeria" };

for (let key in user) {
    console.log(key + ": " + user[key]);
}

```

✅ **Use Case**: Looping through an **object's properties**.

### **6. Loop Control Statements**

**break and continue**

- **`break`** → Stops the loop immediately (**Stop Loop Early)**
- **`continue`** → Skips **one iteration** and moves to the next **(Skip to Next Iteration)**

```jsx
for (let i = 1; i <= 5; i++) {
    if (i === 3) {
        break; // Stops at 3
    }
    console.log(i);
}

```

✔ Exits the loop **immediately** when `i === 3`.

✅ **Use Case**: Stopping a loop when a condition is met.

```jsx
for (let i = 1; i <= 5; i++) {
    if (i === 3) {
        continue; // Skips 3
    }
    console.log(i);
}

```

✔ **Skips** only the current iteration and **continues** the loop.

✅ **Use Case**: Skipping a specific value in a loop.

### **Summary**

| Loop Type | Use Case |
| --- | --- |
| `for` | Runs a set number of times |
| `while` | Runs while a condition is true |
| `do...while` | Runs at least once, then repeats if true |
| `for...of` | Loops through an array |
| `for...in` | Loops through an object |
| `break` | Stops the loop |
| `continue` | Skips an iteration |

Loops **save time** and make code more efficient! 🚀

### More Examples

### **✅ Counting Down a Timer (while loop)**

```
js
CopyEdit
let time = 5;

while (time > 0) {
  console.log(`Time left: ${time}s`);
  time--;
}
console.log("Time's up!");

```

---

### **✅ Finding Even Numbers (for loop & continue)**

```
js
CopyEdit
for (let i = 1; i <= 10; i++) {
  if (i % 2 !== 0) {
    continue; // Skip odd numbers
  }
  console.log("Even number:", i);
}

```