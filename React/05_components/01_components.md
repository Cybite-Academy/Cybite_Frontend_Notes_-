# **React Components - Simple Tutorial & Use Cases**

Components are the **building blocks** of React apps. Think of them like LEGO pieces - you combine them to build complex UIs. Let's break them down simply.

## **What is a Component?**
A component is a **reusable piece of UI** that:
- Contains its own **structure (HTML)**
- Has its own **logic (JavaScript)**
- Can manage its own **state (data)**
- Receives data via **props**

---

## **2 Types of Components**
### 1. **Function Components (Modern)**
```jsx
function Welcome() {
  return <h1>Hello World!</h1>;
}
```

### 2. **Class Components (Older)**
```jsx
class Welcome extends React.Component {
  render() {
    return <h1>Hello World!</h1>;
  }
}
```

*Today, we mostly use **function components** with **hooks**.*

---

## **Component Use Cases with Examples**

### 1️⃣ **Button Component (Reusable UI)**
```jsx
function Button({ text, color }) {
  return (
    <button style={{ backgroundColor: color }}>
      {text}
    </button>
  );
}

// Usage
<Button text="Click Me" color="blue" />
<Button text="Delete" color="red" />
```

### 2️⃣ **Profile Card (Combining Components)**
```jsx
function ProfileCard({ name, job, image }) {
  return (
    <div className="card">
      <Avatar image={image} />
      <h3>{name}</h3>
      <p>{job}</p>
    </div>
  );
}

// Usage
<ProfileCard 
  name="Sarah" 
  job="Web Developer" 
  image="sarah.jpg"
/>
```

### 3️⃣ **Todo List (Stateful Component)**
```jsx
function TodoList() {
  const [todos, setTodos] = useState([
    "Buy milk",
    "Walk the dog"
  ]);

  return (
    <ul>
      {todos.map((todo) => (
        <li key={todo}>{todo}</li>
      ))}
    </ul>
  );
}
```

### 4️⃣ **Modal Popup (Conditional Rendering)**
```jsx
function App() {
  const [showModal, setShowModal] = useState(false);

  return (
    <div>
      <button onClick={() => setShowModal(true)}>
        Open Modal
      </button>
      
      {showModal && (
        <Modal onClose={() => setShowModal(false)}>
          <h2>Welcome!</h2>
          <p>This is a popup message.</p>
        </Modal>
      )}
    </div>
  );
}
```

### 5️⃣ **Theme Switcher (Context API)**
```jsx
function App() {
  const [theme, setTheme] = useState("light");

  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      <Header />
      <MainContent />
      <ThemeToggle />
    </ThemeContext.Provider>
  );
}

// Child component
function ThemeToggle() {
  const { theme, setTheme } = useContext(ThemeContext);
  
  return (
    <button onClick={() => setTheme(
      theme === "light" ? "dark" : "light"
    )}>
      Toggle Theme
    </button>
  );
}
```

---

## **Component Best Practices**
1. **Single Responsibility** - Each component should do one thing
2. **Reusable** - Design components to be reused
3. **Proper Naming** - Use clear names (`UserProfile`, not `Comp1`)
4. **Props Validation** - Use PropTypes or TypeScript
5. **Folder Structure** - Organize components logically

```
/src
  /components
    /Button
      Button.jsx
      Button.css
    /Card
      Card.jsx
      Card.css
```

---

## **When to Create New Components?**
✅ When UI piece is **reused**  
✅ When logic becomes **complex**  
✅ When you need **isolated state**  
✅ When design requires **conditional rendering**

---

## **Real-World Component Examples**
- **Header/Navigation** (reused on every page)
- **Product Card** (repeated in e-commerce listings)
- **Form Input** (reusable with validation)
- **Loading Spinner** (used while data fetches)
- **Error Message** (consistent error display)

---

## **Summary**
- Components = **UI building blocks**
- Can be **simple or complex**
- Make code **organized & reusable**
- Combine **state, props, and logic**

Try building these components in your next project! Which one will you start with? 😊