### 🔁 Ways to Loop Through Objects in JavaScript

---

### 1. **`for...in` loop** – Loop through **keys**

```js
let user = {
  name: "Ada",
  age: 22,
  country: "Nigeria"
};

for (let key in user) {
  console.log(key + ": " + user[key]);
}
```

**Output:**
```
name: Ada
age: 22
country: Nigeria
```

---

### 2. **`Object.keys()` + `forEach()`** – Loop through **keys**

```js
let product = {
  title: "Phone",
  price: 300,
  inStock: true
};

Object.keys(product).forEach((key) => {
  console.log(`${key}: ${product[key]}`);
});
```

---

### 3. **`Object.values()`** – Loop through **values only**

```js
let scores = {
  Math: 85,
  English: 78,
  Science: 92
};

Object.values(scores).forEach((value) => {
  console.log(value);
});
```

---

### 4. **`Object.entries()`** – Loop through **[key, value]** pairs

```js
let movie = {
  title: "Black Panther",
  year: 2018
};

for (let [key, value] of Object.entries(movie)) {
  console.log(`${key}: ${value}`);
}
```

---

### ✅ Real-Life Use Case Examples

1. **Displaying user details on a profile page**

```js
let profile = {
  name: "Emeka",
  age: 30,
  location: "Abuja"
};

for (let key in profile) {
  // You can dynamically build a profile section
  console.log(`Your ${key} is ${profile[key]}`);
}
```

2. **Creating table rows from object data**

```js
let studentScores = {
  Bola: 75,
  Sade: 88,
  Tunde: 95
};

for (let [name, score] of Object.entries(studentScores)) {
  console.log(`${name}: ${score}`);
}
```

---

Let me know if you'd like to see how to loop through an **array of objects**, or how to **filter** or **transform** object values.