## 💡 What is an Object in JavaScript?

An **object** is a way to store **related data and behavior** (values and functions) in a single place.

Think of it like a **real-world thing** — like a **person**, **car**, or **product** — with **characteristics (properties)** and **things it can do (methods)**.

---

### 🧱 Basic Structure of an Object

```js
const person = {
  name: "John",
  age: 30,
  isStudent: false,
};
```

- `person` is the **object**
- `name`, `age`, `isStudent` are **keys (properties)**
- `"John"`, `30`, `false` are the **values**

👉 We call this a **key-value pair**

<br>

### 🔍 How to Access Object Data

```js
console.log(person.name); // Output: John
console.log(person["age"]); // Output: 30
```

✅ Two ways:

1. Dot notation → `person.name`
2. Bracket notation → `person["name"]`

<br>

### ✍️ How to Change Object Data

```js
person.age = 31;
person["isStudent"] = true;
```

<br>

### ➕ How to Add New Properties

```js
person.country = "Nigeria";
```

<br>

### ❌ How to Delete a Property

```js
delete person.isStudent;
```

<br>
<br>

### ⚙️ Object with Functions (Methods)

Objects can have functions too!

```js
const user = {
  name: "Ada",
  greet: function () {
    console.log("Hello, " + this.name + "!");
  },
};

user.greet(); // Output: Hello, Ada!
```

<br>
<br>
<br>
<br>

## ✅ Real-Life Use Case Scenarios


### 📱 1. **User Profile in a Web App**

```js
const userProfile = {
  username: "gamingQueen",
  email: "queen@example.com",
  age: 21,
  isOnline: true,
};
```

Used to store each user's data in apps like Facebook, Instagram, or your esports platform.

---

### 🛒 2. **Product in an Online Store**

```js
const product = {
  id: 123,
  name: "Wireless Headphones",
  price: 20000,
  inStock: true,
};
```

Used in e-commerce platforms to manage products and show them to buyers.

---

### 📦 3. **Order in a Delivery App**

```js
const order = {
  orderId: "ORD-001",
  items: ["Burger", "Fries"],
  totalAmount: 5000,
  delivered: false,
};
```

Used in food and delivery apps to track order status and details.

---

### 📊 4. **Analytics Data**

```js
const analytics = {
  pageViews: 1000,
  users: 350,
  location: "Nigeria",
};
```

Used to show app or website statistics.

---

### ⚙️ 5. **App Settings**

```js
const settings = {
  darkMode: true,
  notifications: false,
  language: "en",
};
```

Used to store user preferences.

---

### 💻 6. **Function Toolkit**

```js
const math = {
  add: (a, b) => a + b,
  multiply: (a, b) => a * b,
};

console.log(math.add(2, 3)); // Output: 5
```

Used to group related functions together for reuse.
<br>
<br>
<br>
<br>

## 🧠 Summary

- An object is a container for storing related data.
- You use it to group things like name, age, or price together.
- Objects are super useful in real apps: for users, products, orders, settings, etc.
