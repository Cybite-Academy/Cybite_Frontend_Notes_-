### 🔹 Why Use Objects? (Use Case Scenarios)

Here are a few **real-world use cases** for using objects in JavaScript:

---

#### ✅ 1. **Storing User Information**
```js
const user = {
  name: "Amaka",
  age: 25,
  email: "amaka@email.com"
};
```
Used in apps to store user profile data.

---

#### ✅ 2. **Representing a Product**
```js
const product = {
  name: "Laptop",
  price: 350000,
  inStock: true
};
```
Used in e-commerce websites to manage product info.

---

#### ✅ 3. **Grouping Functions and Data (Methods)**
```js
const calculator = {
  add: function(a, b) {
    return a + b;
  },
  subtract: function(a, b) {
    return a - b;
  }
};

console.log(calculator.add(5, 3)); // Output: 8
```
Used in apps to organize functions.

---

#### ✅ 4. **API Response Data**
When you fetch data from a server, it often comes as an object:
```js
const response = {
  status: 200,
  message: "Success",
  data: {
    id: 1,
    name: "Book"
  }
};
```

---

#### ✅ 5. **Configuration Settings**
```js
const config = {
  darkMode: true,
  language: "en",
  notifications: false
};
```
Used to store settings in web or mobile apps.

