# **useState Hook - Simple Tutorial with Practical Use Cases**

## **What is useState?**
`useState` is a React Hook that lets you add **state** to functional components. It's the simplest way to make your components remember and manage changing data.

### **Basic Syntax**
```jsx
import { useState } from 'react';

const [state, setState] = useState(initialValue);
```
- `state`: Current value
- `setState`: Function to update the value
- `initialValue`: Starting value (can be any type)

---

## **5 Practical Use Cases**

### 1️⃣ **Counter App (Basic State)**
```jsx
function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>+</button>
      <button onClick={() => setCount(count - 1)}>-</button>
    </div>
  );
}
```
**When to use:** Simple number tracking (likes, votes, quantities)

---

### 2️⃣ **Form Input Handling**
```jsx
function LoginForm() {
  const [email, setEmail] = useState("");
  const [password, setPassword] = useState("");

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log({ email, password });
  };

  return (
    <form onSubmit={handleSubmit}>
      <input 
        type="email" 
        value={email}
        onChange={(e) => setEmail(e.target.value)} 
      />
      <input
        type="password"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
      />
      <button type="submit">Login</button>
    </form>
  );
}
```
**When to use:** Any form inputs (login, search, contact forms)

---

### 3️⃣ **Toggle Switch (Boolean State)**
```jsx
function Toggle() {
  const [isOn, setIsOn] = useState(false);

  return (
    <div>
      <button 
        onClick={() => setIsOn(!isOn)}
        style={{ background: isOn ? "green" : "gray" }}
      >
        {isOn ? "ON" : "OFF"}
      </button>
      {isOn && <p>The switch is ON!</p>}
    </div>
  );
}
```
**When to use:** Toggle buttons, dark mode switches, show/hide elements

---

### 4️⃣ **Todo List (Array State)**
```jsx
function TodoApp() {
  const [todos, setTodos] = useState(["Buy milk", "Walk dog"]);
  const [newTodo, setNewTodo] = useState("");

  const addTodo = () => {
    setTodos([...todos, newTodo]);
    setNewTodo("");
  };

  return (
    <div>
      <input
        value={newTodo}
        onChange={(e) => setNewTodo(e.target.value)}
      />
      <button onClick={addTodo}>Add</button>
      
      <ul>
        {todos.map((todo, index) => (
          <li key={index}>{todo}</li>
        ))}
      </ul>
    </div>
  );
}
```
**When to use:** Lists where items are added/removed (shopping carts, task managers)

---

### 5️⃣ **Object State (User Profile)**
```jsx
function UserProfile() {
  const [user, setUser] = useState({
    name: "Alice",
    age: 25,
    email: "alice@example.com"
  });

  const updateName = () => {
    setUser({ ...user, name: "Bob" });
  };

  return (
    <div>
      <h2>{user.name}</h2>
      <p>Age: {user.age}</p>
      <p>Email: {user.email}</p>
      <button onClick={updateName}>Change Name</button>
    </div>
  );
}
```
**When to use:** When multiple related values need to be grouped (user data, settings)

---

## **Important Notes**
1. **State Updates are Asynchronous**
   ```jsx
   // Wrong
   setCount(count + 1);
   setCount(count + 1); // Won't work as expected

   // Correct (using previous state)
   setCount(prevCount => prevCount + 1);
   setCount(prevCount => prevCount + 1);
   ```

2. **Initial State with Function (Lazy Initialization)**
   ```jsx
   // Runs only on first render
   const [data, setData] = useState(() => {
     const initialValue = calculateExpensiveValue();
     return initialValue;
   });
   ```

3. **State vs Props**
   - Use **state** for data that changes within the component
   - Use **props** for data passed from parent components

---

## **When NOT to Use useState**
❌ For complex state logic (use `useReducer` instead)  
❌ When state needs to be shared across many components (use Context API)  
❌ For derived values (calculate them during rendering instead)  

---

## **Real-World Examples**
- **E-commerce:** Product quantity selector
- **Social Media:** Like button with counter
- **Dashboard:** Theme preference toggle
- **Game:** Score tracking
- **Form Wizard:** Multi-step form progression

---

**Try this exercise:** Create a color picker component that:
1. Shows the current color
2. Has buttons to change between 3 colors
3. Displays the color name

```jsx
function ColorPicker() {
  const colors = ["red", "green", "blue"];
  const [currentColor, setCurrentColor] = useState("red");

  return (
    <div>
      <div style={{
        width: "100px",
        height: "100px",
        backgroundColor: currentColor
      }}></div>
      {colors.map(color => (
        <button 
          key={color} 
          onClick={() => setCurrentColor(color)}
        >
          {color}
        </button>
      ))}
    </div>
  );
}
```

`useState` is your gateway to making interactive React apps! What will you build first? 🚀