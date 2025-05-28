# **Props in React - Simple Tutorial & Use Cases**

Props (short for "properties") are how React components talk to each other. They let you pass data from a parent component to a child component, making your components reusable and dynamic.

---

## **What Are Props?**

- **Like function arguments**, but for components
- **One-way data flow** (parent → child)
- **Read-only** (child can't modify props)
- Can pass **strings, numbers, arrays, objects, functions, even other components!**

---

## **Basic Props Example**

### Parent Component (Sending props)

```jsx
function App() {
  return <WelcomeMessage name="Alice" age={25} />;
}
```

### Child Component (Receiving props)

```jsx
function WelcomeMessage(props) {
  return (
    <h1>
      Hello, {props.name}! You are {props.age} years old.
    </h1>
  );
}
```

**Output:**  
`Hello, Alice! You are 25 years old.`

### Alternative (Destructuring Props)

```jsx
function WelcomeMessage({ name, age }) {
  return (
    <h1>
      Hello, {name}! You are {age} years old.
    </h1>
  );
}
```

---

## **Common Use Cases with Examples**

### 1️⃣ **Reusable UI Components (Buttons, Cards)**

```jsx
// Parent
<Button color="blue" text="Click Me" />;

// Child (Button.js)
function Button({ color, text }) {
  return <button style={{ backgroundColor: color }}>{text}</button>;
}
```

### 2️⃣ **Dynamic Lists (Todo Items, Product Cards)**

```jsx
// Parent
<TodoList todos={["Buy milk", "Walk dog", "Code React"]} />;

// Child (TodoList.js)
function TodoList({ todos }) {
  return (
    <ul>
      {todos.map((task) => (
        <li key={task}>{task}</li>
      ))}
    </ul>
  );
}
```

### 3️⃣ **Conditional Rendering (Show/Hide Content)**

```jsx
// Parent
<Greeting isLoggedIn={true} />;

// Child (Greeting.js)
function Greeting({ isLoggedIn }) {
  return isLoggedIn ? <p>Welcome back!</p> : <p>Please login</p>;
}
```

### 4️⃣ **Passing Functions (Child to Parent Communication)**

```jsx
// Parent
function App() {
  const handleClick = () => alert("Button clicked!");
  return <ChildComponent onButtonClick={handleClick} />;
}

// Child
function ChildComponent({ onButtonClick }) {
  return <button onClick={onButtonClick}>Click Me</button>;
}
```

### 5️⃣ **Component Composition (Passing Components as Props)**

```jsx
// Parent
<Layout header={<Header />} content={<MainContent />} footer={<Footer />} />;

// Child (Layout.js)
function Layout({ header, content, footer }) {
  return (
    <div>
      <div>{header}</div>
      <main>{content}</main>
      <div>{footer}</div>
    </div>
  );
}
```

---

## **Props vs State**

| Feature        | Props          | State                 |
| -------------- | -------------- | --------------------- |
| **Ownership**  | Parent → Child | Internal to component |
| **Mutability** | Read-only      | Can be changed        |
| **Use Case**   | Configuration  | Dynamic data          |

---

## **When NOT to Use Props**

- When data needs to **change internally** (use **state**)
- When passing through **many layers** (use **Context API** instead)
- When components are **siblings** (lift state up to parent)

---

## **Real-World Example: User Profile Card**

```jsx
// Parent
<UserProfile
  name="Sarah"
  role="Developer"
  avatarUrl="/sarah.jpg"
  onFollow={() => console.log("Followed!")}
/>;

// Child
function UserProfile({ name, role, avatarUrl, onFollow }) {
  return (
    <div className="profile-card">
      <img src={avatarUrl} alt={name} />
      <h2>{name}</h2>
      <p>{role}</p>
      <button onClick={onFollow}>Follow</button>
    </div>
  );
}
```

---

## **Summary**

✅ Props = **Parent-to-child communication**  
✅ Make components **reusable**  
✅ Can pass **any data type**  
❌ Don't modify props – they're **read-only**
