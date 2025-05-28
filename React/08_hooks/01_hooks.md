# **React Hooks - Simple Explanation & Practical Use Cases**

Hooks are special functions that let you "hook into" React features from function components. They make React code cleaner and easier to understand compared to class components.

## **Why Hooks?**

- Add state to functional components
- Replace lifecycle methods
- Reuse stateful logic between components
- Make your code more readable and organized

---

## **Most Common Hooks & Use Cases**

### 1️⃣ **useState (State Management)**

**What it does:** Lets you add state to functional components.

**Use Case:** Form inputs, counters, toggle switches

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

### 2️⃣ **useEffect (Side Effects)**

**What it does:** Handles side effects (API calls, subscriptions, DOM manipulations).

**Use Cases:**

- Fetching data
- Setting up event listeners
- Updating DOM when state changes

```jsx
import { useState, useEffect } from "react";

function UserProfile({ userId }) {
  const [user, setUser] = useState(null);

  useEffect(() => {
    fetch(`/api/users/${userId}`)
      .then((res) => res.json())
      .then((data) => setUser(data));
  }, [userId]); // Runs when userId changes

  if (!user) return <p>Loading...</p>;

  return <h1>{user.name}</h1>;
}
```

### 3️⃣ **useContext (Global State)**

**What it does:** Accesses context without nesting.

**Use Case:** Theme switching, user authentication

```jsx
import { createContext, useContext } from "react";

const ThemeContext = createContext("light");

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <Toolbar />
    </ThemeContext.Provider>
  );
}

function Toolbar() {
  const theme = useContext(ThemeContext);
  return (
    <button style={{ background: theme === "dark" ? "#333" : "#FFF" }}>
      Themed Button
    </button>
  );
}
```

### 4️⃣ **useRef (Persistent Values)**

**What it does:** Creates mutable ref objects that persist between renders.

**Use Cases:**

- Accessing DOM elements
- Storing previous values
- Keeping track of intervals

```jsx
import { useRef, useEffect } from "react";

function TextInputWithFocus() {
  const inputRef = useRef(null);

  useEffect(() => {
    inputRef.current.focus(); // Auto-focus on mount
  }, []);

  return <input ref={inputRef} type="text" />;
}
```

### 5️⃣ **useReducer (Complex State)**

**What it does:** Alternative to useState for complex state logic.

**Use Case:** Shopping carts, form state management

```jsx
import { useReducer } from "react";

function reducer(state, action) {
  switch (action.type) {
    case "increment":
      return { count: state.count + 1 };
    case "decrement":
      return { count: state.count - 1 };
    default:
      throw new Error();
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, { count: 0 });

  return (
    <div>
      Count: {state.count}
      <button onClick={() => dispatch({ type: "increment" })}>+</button>
      <button onClick={() => dispatch({ type: "decrement" })}>-</button>
    </div>
  );
}
```

### 6️⃣ **Custom Hooks (Reusable Logic)**

**What it does:** Lets you extract component logic into reusable functions.

**Use Case:** Form handling, API fetching

```jsx
function useToggle(initialState = false) {
  const [state, setState] = useState(initialState);
  const toggle = () => setState(!state);
  return [state, toggle];
}

function Switch() {
  const [isOn, toggleIsOn] = useToggle(false);

  return <button onClick={toggleIsOn}>{isOn ? "ON" : "OFF"}</button>;
}
```

---

## **When to Use Which Hook?**

| Hook         | Best For                      |
| ------------ | ----------------------------- |
| `useState`   | Basic state management        |
| `useEffect`  | Side effects, data fetching   |
| `useContext` | Accessing global state        |
| `useRef`     | DOM access, persistent values |
| `useReducer` | Complex state logic           |
| Custom Hooks | Reusable component logic      |

---

## **Real-World Hook Combinations**

1. **Form Handling**

```jsx
function useForm(initialValues) {
  const [values, setValues] = useState(initialValues);

  const handleChange = (e) => {
    setValues({
      ...values,
      [e.target.name]: e.target.value,
    });
  };

  return [values, handleChange];
}

function LoginForm() {
  const [form, handleChange] = useForm({ email: "", password: "" });

  return (
    <form>
      <input name="email" value={form.email} onChange={handleChange} />
      <input name="password" value={form.password} onChange={handleChange} />
    </form>
  );
}
```

2. **API Fetching**

```jsx
function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((data) => {
        setData(data);
        setLoading(false);
      });
  }, [url]);

  return { data, loading };
}

function UserProfile({ userId }) {
  const { data: user, loading } = useFetch(`/users/${userId}`);

  if (loading) return <p>Loading...</p>;
  return <h1>{user.name}</h1>;
}
```

---

## **Key Rules of Hooks**

1. Only call hooks at the **top level** (not in loops/conditions)
2. Only call hooks from **React function components**
3. Name custom hooks starting with "use" (e.g., `useForm`)

---

Hooks make React development cleaner and more powerful. Start with `useState` and `useEffect`, then explore others as you need them!
